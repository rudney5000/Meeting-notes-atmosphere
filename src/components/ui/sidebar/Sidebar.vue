<script setup lang="ts">
    import {
    Select,
    SelectContent,
    SelectGroup,
    SelectItem,
    SelectLabel,
    SelectTrigger,
    SelectValue,
    } from '@/components/ui/select'
</script>

<template>
    <div class="hidden sm:block sm:col-span-1 relative border-r  border-gray-300">
        <div class="flex sm:bg-transparent p-2 sm:p-0 w-full">
            <div class="block relative w-full">
                <h2 class="mb-2 px-4 text-lg font-semibold tracking-tight">Cultes</h2>
                <Select>
                    <SelectTrigger class="w-[180px]">
                    <SelectValue placeholder="Select a fruit" />
                    </SelectTrigger>
                    <SelectContent>
                    <SelectGroup>
                        <SelectLabel>Fruits</SelectLabel>
                        <SelectItem value="apple">
                        Apple
                        </SelectItem>
                        <SelectItem value="banana">
                        Banana
                        </SelectItem>
                        <SelectItem value="blueberry">
                        Blueberry
                        </SelectItem>
                        <SelectItem value="grapes">
                        Grapes
                        </SelectItem>
                        <SelectItem value="pineapple">
                        Pineapple
                        </SelectItem>
                    </SelectGroup>
                    </SelectContent>
                </Select>
                <div class="mt-2 m-6">
                    <router-link
                        to="notes"
                        class="flex items-center px-4 py-2 tracking-wide text-gray-700 rounded-r-full outline-none cursor-pointer select-none"
                    >
                        <f-icon icon="file-alt"/>
                        <span class="ml-4">Cantiques</span>
                        <span
                        class="px-2 py-1 ml-auto text-xs font-medium leading-none bg-gray-300 rounded-full"
                        >
                        0001
                        </span>
                    </router-link>
                    <router-link
                        to="notes"
                        class="flex items-center px-4 py-2 tracking-wide text-gray-700 rounded-r-full outline-none cursor-pointer select-none"
                    >
                        <f-icon icon="file-alt"/>
                        <span class="ml-4">Cantiques</span>
                        <span
                        class="px-2 py-1 ml-auto text-xs font-medium leading-none bg-gray-300 rounded-full"
                        >
                        0002
                        </span>
                    </router-link>
                    <router-link
                        to="notes"
                        class="flex items-center px-4 py-2 tracking-wide text-gray-700 rounded-r-full outline-none cursor-pointer select-none"
                    >
                        <f-icon icon="file-alt"/>
                        <span class="ml-4">Cantiques</span>
                        <span
                        class="px-2 py-1 ml-auto text-xs font-medium leading-none bg-gray-300 rounded-full"
                        >
                        0003
                        </span>
                    </router-link>
                    <router-link
                        to="notes"
                        class="flex items-center px-4 py-2 tracking-wide text-gray-700 rounded-r-full outline-none cursor-pointer select-none"
                    >
                        <f-icon icon="file-alt"/>
                        <span class="ml-4">Cantiques</span>
                        <span
                        class="px-2 py-1 ml-auto text-xs font-medium leading-none bg-gray-300 rounded-full"
                        >
                        0004
                        </span>
                    </router-link>
                </div>
            </div>
        </div>
    </div>
</template>