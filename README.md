<center>
![image](https://vuejs.org/images/logo.svg)
# Vue JS
</center>
## What is Vue.js? [pronounced /vjuː/, like view]

Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces. Easy to learn. It required only basic knowledge of HTML, CSS and JS only. It has easiest learning Curved among other frame-works out there.

## Structure 
```
<template>     // responsible for view.
</template>

<script>        // where business logic can be written
    export default {

    }
</script>

<style scoped?> // scoped : property states that given style are 
</style> // only apply on current component otherwise it's global

```
## LifeCycle
Like react JS vue has life cycle methods too.

It represent by 4 phase of component load. Vue has 13 life cycle methods. but most often 8 life cycle methods are used

<style>
    table {
        text-align: center;
        width: 100%;
        border: 1px solid;
    }

    th {
        text-align: center;
    }

    th:first-child {
        text-align: left;
    }



    td:first-child {
        text-align: left;
    }
</style>


Phase|LifeCycle methods
--- | --- 
Creation | beforeCreate(), created()
Mounting | beforeMount(), mounted()
Updating | beforeUpdate(), updated()
Unmounting | beforeUnmount(), unmounted()
MISC | activated(), deactivated(), errorCaptured(), renderTracked(), renderTriggered()


## Vue Directives [Attributes]

>  tip:  
> - data is same as state in React
> - `<template>` tag is same as `<React.Fragment>`

<br>

# | Directive | Shorthand | Example | Use | Extra
--- | --- | --- | --- | --- | --- 
1 | `v-bind:<attribute-name>` | `:<attribute-name>` | <div> `<input type="text" v-bind:value="f_name">  or  <input type="text" :value="f_name">`</div> | Dynamically bind attribute on Component. trim: same as value.trim(). lazy: set data on lose focus | `<input type="text" v-bind:value.trim.lazy="f_name">`
2 | `v-model` | - | `<input type="text" v-model="f_name">` | Bind data [State] with view. v  |  `<input type="text" v-model.trim="f_name"> or <input type="text" v-model.trim.lazy="f_name">`  
3 | `v-text`| - | `<div v-text="Text" />`| Dynamically bind text value on component | -
4 | `v-html`| - | `<div v-html="<h2>Text</h2>" />`| Dynamically bind HTML on component | -
5 | `v-for`| - |`<template v-for="(item, index )in items" > </template>`| Use to iterate List in Vue. while using v-for we must have to asign v-bind:key same as we asign in React | - 
6 | `v-show` | - | `<div v-show="shouldShow" ></div` | Conditionally render Component | -
7 | `v-if` | - | `<div v-if="<condition>"></div>` | Conditionally render Element | -
8 | `v-elseif` | - | `<div v-elseif="<condition>"></div>` | Nested if  | - 
9 | `v-else` | -  |`<div v-else></div>`| else part | -
10 | `v-pre` | - | `<div v-pre>>{{ dynamicValue }}</div>` | This is renders `{{ dynamicValue }}` instead of actual dynamic value | -
11 | `v-once` | - | `<div v-once> </div>` | This ensures that element renders Once | -
 
 </br>

## Modifiers

# | Modifier | example | use
--- | --- | --- | ---
1 | .trim | `<input type="text" name="f_name" v-model.trim="f_name" />` | This will ignore white-space in input so no need to take care of blank data.
2 | .lazy | `<input type="text" name="f_name" v-model.lazy="f_name" />` | This will ensure input change not cause re-render onChange of input, it will reflect on state after input focus lose.
3 | .number | `<input type="number" name="age" v-model.number="age" />` | This will add input text number in state.
4 | .prevent | `<form v-on:submit.prevent="submitForm()"></form>` | This is act as event.preventDefault() in submit form event. vue  will automatically invoke preventDefault by using .prevent modifier.
5 | key modifier | `<button @keyup.enter="eventHandler">Button</button>` | Key modifier provide all keys including [ enter, alt, cntl, shift, .. etc. ]