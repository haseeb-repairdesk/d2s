<template>
    <div class="dd-w-full dd-bg-white">
        <dd-checkbox />
        <svgIcon icon="Alert" />
        <Badge />
        <Actions :buttons="buttons" :showIcon="showIcon" />
    </div>
</template>

<script setup>
import { ref } from "vue";
import DdCheckbox from "../checkbox/index.vue"
import svgIcon from "../svgIcon/index.vue"
import Badge from "./Badge.vue";
import Actions from "./Actions.vue";

const showIcon = ref(true);
const buttons = ref([
    { id: 1, label: "Button 1", color: "white", icon: "ChevronLeft" },
    { id: 2, label: "Button 2", color: "primary", icon: "ChevronRight" },
    { id: 3, label: "Button 3", color: "danger", icon: "ChevronDown" },
    { id: 4, label: "Button 4", color: "warning", icon: "ChevronLeft" },
    { id: 5, label: "Button 5", color: "selected", icon: "ChevronRight" },
    { id: 6, label: "", size: "xs", color: "white", icon: "ChevronUp" },
    { id: 7, label: "", size: "xl", color: "white", icon: "ChevronDown" },
    //add more buttons here use same props as defined in dd-button
]);
const treeItem = [
    {
        id: 0, label: "All Categories", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
            {
                id: 0, label: "Computer", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                    {
                        id: 0, label: "Laptops", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                            {
                                id: 0, label: "Macbook", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                                    { id: 0, label: "Pro", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Air", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Pro M1", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Air M1", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                ]
                            },
                            {
                                id: 0, label: "PC", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                                    { id: 0, label: "XPS", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Zenbook", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Lenovo X1 Carbon", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                ]
                            },
                        ]
                    },
                    { id: 0, label: "Desktop", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                ]
            },
        ]
    },
    {
        id: 1, label: "Mobile", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
            {
                id: 0, label: "Iphone", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                    {
                        id: 0, label: "IphoneX and below...", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                            {
                                id: 0, label: "Iphone X", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                                    { id: 0, label: "Screen repair", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Camera repair", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Cleaning", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Wifi signal issue", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                ]
                            },
                            {
                                id: 0, label: "Iphone 6", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [
                                    { id: 0, label: "Screen repair", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Camera repair", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Cleaning", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                    { id: 0, label: "Wifi signal issue", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                                ]
                            },
                        ]
                    },
                    { id: 0, label: "Iphone 11 and above models", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
                ]
            },
            { id: 0, label: "Andriod", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
        ]
    },
    { id: 2, label: "Watch", icon: "", checkbox: true, checked: true, badge: true, actions: true, disabled: false, children: [] },
]
</script>

<style scoped></style>