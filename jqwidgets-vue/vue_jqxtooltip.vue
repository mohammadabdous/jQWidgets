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
    import '../jqwidgets/jqxtooltip.js';

    export default {
        props: {
            absolutePositionX: Number,
            absolutePositionY: Number,
            autoHide: Boolean,
            autoHideDelay: Number,
            animationShowDelay: Number,
            animationHideDelay: Number,
            content: String,
            closeOnClick: Boolean,
            disabled: Boolean,
            enableBrowserBoundsDetection: Boolean,
            height: [Number, String],
            left: Number,
            name: String,
            opacity: Number,
            position: String,
            rtl: Boolean,
            showDelay: Number,
            showArrow: Boolean,
            top: Number,
            trigger: String,
            theme: String,
            width: [Number, String],
            autoCreate: {
                default: true,
                type: Boolean
            }
        },
        created: function () {
            this.id = 'jqxTooltip' + JQXLite.generateID();
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
                JQXLite(this.componentSelector).jqxTooltip(options);
            },
            getOptions: function () {
                const usedProps = Object.keys(this.__manageProps__());
                const resultToReturn = {};
                for (let i = 0; i < usedProps.length; i++) {
                    resultToReturn[usedProps[i]] = JQXLite(this.componentSelector).jqxTooltip(usedProps[i]);
                }
                return resultToReturn;
            },
            close: function(index) {
                JQXLite(this.componentSelector).jqxTooltip('close', index);  
            },
            destroy: function() {
                JQXLite(this.componentSelector).jqxTooltip('destroy');  
            },
            open: function(left, top) {
                JQXLite(this.componentSelector).jqxTooltip('open', left, top);  
            },
            refresh: function() {
                JQXLite(this.componentSelector).jqxTooltip('refresh');  
            },
            _absolutePositionX: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('absolutePositionX', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('absolutePositionX');
                }
            },
            _absolutePositionY: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('absolutePositionY', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('absolutePositionY');
                }
            },
            _autoHide: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('autoHide', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('autoHide');
                }
            },
            _autoHideDelay: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('autoHideDelay', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('autoHideDelay');
                }
            },
            _animationShowDelay: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('animationShowDelay', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('animationShowDelay');
                }
            },
            _animationHideDelay: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('animationHideDelay', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('animationHideDelay');
                }
            },
            _content: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('content', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('content');
                }
            },
            _closeOnClick: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('closeOnClick', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('closeOnClick');
                }
            },
            _disabled: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('disabled', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('disabled');
                }
            },
            _enableBrowserBoundsDetection: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('enableBrowserBoundsDetection', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('enableBrowserBoundsDetection');
                }
            },
            _height: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('height', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('height');
                }
            },
            _left: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('left', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('left');
                }
            },
            _name: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('name', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('name');
                }
            },
            _opacity: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('opacity', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('opacity');
                }
            },
            _position: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('position', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('position');
                }
            },
            _rtl: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('rtl', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('rtl');
                }
            },
            _showDelay: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('showDelay', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('showDelay');
                }
            },
            _showArrow: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('showArrow', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('showArrow');
                }
            },
            _top: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('top', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('top');
                }
            },
            _trigger: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('trigger', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('trigger');
                }
            },
            _theme: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('theme', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('theme');
                }
            },
            _width: function(arg) {
                if (arg !== undefined) {
                    JQXLite(this.componentSelector).jqxTooltip('width', arg)
                } else {
                    return JQXLite(this.componentSelector).jqxTooltip('width');
                }
            },
            __createComponent__: function (options) {
                let widgetOptions;
                options ? widgetOptions = options : widgetOptions = this.__manageProps__();
                JQXLite(this.componentSelector).jqxTooltip(widgetOptions);
                this.__extendProps__();
                this.__wireEvents__();
            },
            __manageProps__: function () {
                const widgetProps = ['absolutePositionX','absolutePositionY','autoHide','autoHideDelay','animationShowDelay','animationHideDelay','content','closeOnClick','disabled','enableBrowserBoundsDetection','height','left','name','opacity','position','rtl','showDelay','showArrow','top','trigger','theme','width'];
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

                Object.defineProperty(that, 'absolutePositionX', {
                    get() {
                        return that._absolutePositionX();
                    },
                    set(newValue) {
                        that._absolutePositionX(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'absolutePositionY', {
                    get() {
                        return that._absolutePositionY();
                    },
                    set(newValue) {
                        that._absolutePositionY(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'autoHide', {
                    get() {
                        return that._autoHide();
                    },
                    set(newValue) {
                        that._autoHide(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'autoHideDelay', {
                    get() {
                        return that._autoHideDelay();
                    },
                    set(newValue) {
                        that._autoHideDelay(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'animationShowDelay', {
                    get() {
                        return that._animationShowDelay();
                    },
                    set(newValue) {
                        that._animationShowDelay(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'animationHideDelay', {
                    get() {
                        return that._animationHideDelay();
                    },
                    set(newValue) {
                        that._animationHideDelay(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'content', {
                    get() {
                        return that._content();
                    },
                    set(newValue) {
                        that._content(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'closeOnClick', {
                    get() {
                        return that._closeOnClick();
                    },
                    set(newValue) {
                        that._closeOnClick(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
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
                Object.defineProperty(that, 'enableBrowserBoundsDetection', {
                    get() {
                        return that._enableBrowserBoundsDetection();
                    },
                    set(newValue) {
                        that._enableBrowserBoundsDetection(newValue);
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
                Object.defineProperty(that, 'left', {
                    get() {
                        return that._left();
                    },
                    set(newValue) {
                        that._left(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'name', {
                    get() {
                        return that._name();
                    },
                    set(newValue) {
                        that._name(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'opacity', {
                    get() {
                        return that._opacity();
                    },
                    set(newValue) {
                        that._opacity(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'position', {
                    get() {
                        return that._position();
                    },
                    set(newValue) {
                        that._position(newValue);
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
                Object.defineProperty(that, 'showDelay', {
                    get() {
                        return that._showDelay();
                    },
                    set(newValue) {
                        that._showDelay(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'showArrow', {
                    get() {
                        return that._showArrow();
                    },
                    set(newValue) {
                        that._showArrow(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'top', {
                    get() {
                        return that._top();
                    },
                    set(newValue) {
                        that._top(newValue);
                    },
                    enumerable: true,
                    configurable: true
                });
                Object.defineProperty(that, 'trigger', {
                    get() {
                        return that._trigger();
                    },
                    set(newValue) {
                        that._trigger(newValue);
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

                JQXLite(this.componentSelector).on('close', function (event) { that.$emit('close', event); });
                JQXLite(this.componentSelector).on('closing', function (event) { that.$emit('closing', event); });
                JQXLite(this.componentSelector).on('open', function (event) { that.$emit('open', event); });
                JQXLite(this.componentSelector).on('opening', function (event) { that.$emit('opening', event); });
            }
        }
    }
</script>
