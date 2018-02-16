```ts
import { AfterViewInit, ElementRef, EventEmitter, OnChanges, SimpleChanges } from '@angular/core';
import { ControlValueAccessor } from '@angular/forms';
export declare class QuillEditorComponent implements AfterViewInit, ControlValueAccessor, OnChanges {
    private elementRef;
    quillEditor: any;
    editorElem: HTMLElement;
    content: any;
    defaultModules: {
        toolbar: (string[] | {
            'header': number;
        }[] | {
            'list': string;
        }[] | {
            'script': string;
        }[] | {
            'indent': string;
        }[] | {
            'direction': string;
        }[] | {
            'size': (string | boolean)[];
        }[] | {
            'header': (number | boolean)[];
        }[] | ({
            'color': any[];
        } | {
            'background': any[];
        })[] | {
            'font': any[];
        }[] | {
            'align': any[];
        }[])[];
    };
    options: Object;
    blur: EventEmitter<any>;
    focus: EventEmitter<any>;
    ready: EventEmitter<any>;
    change: EventEmitter<any>;
    onModelChange: Function;
    onModelTouched: Function;
    constructor(elementRef: ElementRef);
    ngAfterViewInit(): void;
    ngOnChanges(changes: SimpleChanges): void;
    writeValue(currentValue: any): void;
    registerOnChange(fn: Function): void;
    registerOnTouched(fn: Function): void;
}
```