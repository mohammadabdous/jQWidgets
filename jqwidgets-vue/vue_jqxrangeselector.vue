/*
jQWidgets v6.1.0 (2018-October)
Copyright (c) 2011-2018 jQWidgets.
License: https://jqwidgets.com/license/
*/
/* eslint-disable */

<template>
    <div v-bind:id="id">
        <slot></slot>
    </div>
</template>

<script>
    import '../jqwidgets/jqxcore.js';
    import '../jqwidgets/jqxdata.js';
    import '../jqwidgets/jqxtooltip.js';
    import '../jqwidgets/jqxrangeselector.js';

    export default {
        props: {
            disabled: Boolean,
            showGroupLabels: Boolean,
            labelsOnTicks: Boolean,
            markersFormatFunction: Function,
            height: [Number, String],
            labelsFormat: String,
            labelsFormatFunction: Function,
            labelPrecision: Number,
            moveOnClick: Boolean,
            markerRenderer: Function,
            markerPrecision: Number,
            majorLabelRenderer: Function,
            markersFormat: String,
            majorTicksInterval: [Number, String, Object],
            minorTicksInterval: [Number, String, Object],
            max: [Number, String, Date],
            min: [Number, String, Date],
            padding: [String, Number],
            range: Object,
            resizable: Boolean,
            rtl: Boolean,
            showMinorTicks: Boolean,
            snapToTicks: Boolean,
            showMajorLabels: Boolean,
            showMarkers: Boolean,
            theme: String,
            width: [Number, String],
            autoCreate: {
                default: true,
                type: Boolean
            }
        },
        created: function () {
            this.id = 'jqxRangeSelector' + JQXLite.generateID();
            this.componentSelector = '#' + this.id;
        },
        mounted: function () {
            if (this.autoCreate) this.__createComponent__();
        },
        methods: {
            createComponent: function (options) {
                if (!this.autoCreate) this.__createComponent__(options)
                else console.warn('Component is already created! If you want to use createComponent, please set "autoCreate" property to "false".');
            },
            setOptions: function (options) {
                JQXLite(this.componentSelector).jqxRangeSelector(options);
            },
            getOptions: function () {
                const usedProps = Object.keys(this.__manageProps__());
                const resultToReturn = {};
                for (let i = 0; i < usedProps.length; i++) {
                    resultToReturn[usedProps[i]] = JQXLite(this.componentSelector).jqxRangeSelector(usedProps[i]);
                }
                return resultToReturn;
            },
            destroy: function() {
                JQXLite(this.componentSelector).jqxRangeSelector('destroy');  
            },
            getRange: function() {
                return JQXLite(this.componentSelector).jqxRangeSelector('getRange');  
            },
            render: function() {
                JQXLite(this.componentSelector).jqxRangeSelector('render');  
            },
            refresh: function() {
                JQXLite(this.componentSelector).jqxRangeSelector('refresh');  
            },
            setRange: function(from, to) {
                JQXLite(this.componentSelector).jqxRangeSelector('setRange', from, to);  
            },
            _disabled: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('disabled', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('disabled');
                }
            },
            _showGroupLabels: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('showGroupLabels', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('showGroupLabels');
                }
            },
            _labelsOnTicks: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('labelsOnTicks', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('labelsOnTicks');
                }
            },
            _markersFormatFunction: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('markersFormatFunction', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('markersFormatFunction');
                }
            },
            _height: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('height', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('height');
                }
            },
            _labelsFormat: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('labelsFormat', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('labelsFormat');
                }
            },
            _labelsFormatFunction: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('labelsFormatFunction', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('labelsFormatFunction');
                }
            },
            _labelPrecision: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('labelPrecision', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('labelPrecision');
                }
            },
            _moveOnClick: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('moveOnClick', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('moveOnClick');
                }
            },
            _markerRenderer: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('markerRenderer', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('markerRenderer');
                }
            },
            _markerPrecision: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('markerPrecision', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('markerPrecision');
                }
            },
            _majorLabelRenderer: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('majorLabelRenderer', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('majorLabelRenderer');
                }
            },
            _markersFormat: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('markersFormat', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('markersFormat');
                }
            },
            _majorTicksInterval: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('majorTicksInterval', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('majorTicksInterval');
                }
            },
            _minorTicksInterval: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('minorTicksInterval', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('minorTicksInterval');
                }
            },
            _max: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('max', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('max');
                }
            },
            _min: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('min', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('min');
                }
            },
            _padding: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('padding', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('padding');
                }
            },
            _range: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('range', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('range');
                }
            },
            _resizable: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('resizable', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('resizable');
                }
            },
            _rtl: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('rtl', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('rtl');
                }
            },
            _showMinorTicks: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('showMinorTicks', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('showMinorTicks');
                }
            },
            _snapToTicks: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('snapToTicks', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('snapToTicks');
                }
            },
            _showMajorLabels: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('showMajorLabels', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('showMajorLabels');
                }
            },
            _showMarkers: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('showMarkers', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('showMarkers');
                }
            },
            _theme: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('theme', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('theme');
                }
            },
            _width: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxRangeSelector('width', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxRangeSelector('width');
                }
            },
            __createComponent__: function (options) {
                let widgetOptions;
                options ? widgetOptions = options : widgetOptions = this.__manageProps__();
                JQXLite(this.componentSelector).jqxRangeSelector(widgetOptions);
                this.__extendProps__();
                this.__wireEvents__();
            },
            __manageProps__: function () {
                const widgetProps = ['disabled','showGroupLabels','labelsOnTicks','markersFormatFunction','height','labelsFormat','labelsFormatFunction','labelPrecision','moveOnClick','markerRenderer','markerPrecision','majorLabelRenderer','markersFormat','majorTicksInterval','minorTicksInterval','max','min','padding','range','resizable','rtl','showMinorTicks','snapToTicks','showMajorLabels','showMarkers','theme','width'];
                const componentProps = this.$options.propsData;
                let options = {};

                for (let prop in componentProps) {
                    if (widgetProps.indexOf(prop) !== -1) {
                        options[prop] = componentProps[prop];
                    }
                }
                return options;
            },
            __extendProps__: function () {
                const that = this;

                Object.defineProperty(that, 'disabled', {
                    get() {
                        return that._disabled();
                    },
                    set(newValue) {
                        that._disabled(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'showGroupLabels', {
                    get() {
                        return that._showGroupLabels();
                    },
                    set(newValue) {
                        that._showGroupLabels(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'labelsOnTicks', {
                    get() {
                        return that._labelsOnTicks();
                    },
                    set(newValue) {
                        that._labelsOnTicks(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'markersFormatFunction', {
                    get() {
                        return that._markersFormatFunction();
                    },
                    set(newValue) {
                        that._markersFormatFunction(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'height', {
                    get() {
                        return that._height();
                    },
                    set(newValue) {
                        that._height(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'labelsFormat', {
                    get() {
                        return that._labelsFormat();
                    },
                    set(newValue) {
                        that._labelsFormat(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'labelsFormatFunction', {
                    get() {
                        return that._labelsFormatFunction();
                    },
                    set(newValue) {
                        that._labelsFormatFunction(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'labelPrecision', {
                    get() {
                        return that._labelPrecision();
                    },
                    set(newValue) {
                        that._labelPrecision(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'moveOnClick', {
                    get() {
                        return that._moveOnClick();
                    },
                    set(newValue) {
                        that._moveOnClick(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'markerRenderer', {
                    get() {
                        return that._markerRenderer();
                    },
                    set(newValue) {
                        that._markerRenderer(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'markerPrecision', {
                    get() {
                        return that._markerPrecision();
                    },
                    set(newValue) {
                        that._markerPrecision(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'majorLabelRenderer', {
                    get() {
                        return that._majorLabelRenderer();
                    },
                    set(newValue) {
                        that._majorLabelRenderer(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'markersFormat', {
                    get() {
                        return that._markersFormat();
                    },
                    set(newValue) {
                        that._markersFormat(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'majorTicksInterval', {
                    get() {
                        return that._majorTicksInterval();
                    },
                    set(newValue) {
                        that._majorTicksInterval(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'minorTicksInterval', {
                    get() {
                        return that._minorTicksInterval();
                    },
                    set(newValue) {
                        that._minorTicksInterval(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'max', {
                    get() {
                        return that._max();
                    },
                    set(newValue) {
                        that._max(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'min', {
                    get() {
                        return that._min();
                    },
                    set(newValue) {
                        that._min(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'padding', {
                    get() {
                        return that._padding();
                    },
                    set(newValue) {
                        that._padding(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'range', {
                    get() {
                        return that._range();
                    },
                    set(newValue) {
                        that._range(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'resizable', {
                    get() {
                        return that._resizable();
                    },
                    set(newValue) {
                        that._resizable(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'rtl', {
                    get() {
                        return that._rtl();
                    },
                    set(newValue) {
                        that._rtl(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'showMinorTicks', {
                    get() {
                        return that._showMinorTicks();
                    },
                    set(newValue) {
                        that._showMinorTicks(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'snapToTicks', {
                    get() {
                        return that._snapToTicks();
                    },
                    set(newValue) {
                        that._snapToTicks(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'showMajorLabels', {
                    get() {
                        return that._showMajorLabels();
                    },
                    set(newValue) {
                        that._showMajorLabels(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'showMarkers', {
                    get() {
                        return that._showMarkers();
                    },
                    set(newValue) {
                        that._showMarkers(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'theme', {
                    get() {
                        return that._theme();
                    },
                    set(newValue) {
                        that._theme(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'width', {
                    get() {
                        return that._width();
                    },
                    set(newValue) {
                        that._width(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
            },
            __wireEvents__: function () {
                const that = this;

                JQXLite(this.componentSelector).on('change', function (event) { that.$emit('change', event); });
            }
        }
    }
</script>
