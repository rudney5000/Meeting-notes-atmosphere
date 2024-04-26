<script setup lang="ts">
    import {
        Select,
        SelectContent,
        SelectGroup,
        SelectItem,
        SelectLabel,
        SelectTrigger,
        SelectValue,
    } from '@/components/ui/select';

    import { Button } from '@/components/ui/button';
    import { ChevronLeftIcon, ChevronRightIcon, DoubleArrowLeftIcon, DoubleArrowRightIcon } from '@radix-icons/vue'

</script>

<template>
    <div class="flex items-center justify-between px-2">
        <div class="flex-2 text-sm text-muted-foreground">
            row(s) selected
        </div>
        <div class="flex items-center space-x-6 lg:space-x-8">
            <div class="flex items-center space-x-2">
                <p class="text-sm font-medium">
                    Row per page
                </p>
                <Select class="text-white">
                    <SelectTrigger class="h-8 w-[70px]">
                        <SelectValue placeholder="10" class="text-black" />
                    </SelectTrigger>
                    <SelectContent side="top">
                        <SelectItem v-for="pageSize in [10, 20, 30, 40, 50]" :key="pageSize" :value="`${pageSize}`">
                            {{ pageSize }}
                        </SelectItem>
                    </SelectContent>
                </Select>
            </div>
            <div class="flex w-[100px] items-center justify-center text-sm font-medium">
                Page 1 of 10
            </div>
            <div class="flex items-center space-x-2">
                <Button
                    variant ="outline"
                    class="hidden h-8 w-8 p-0 lg:flex"
                >
                    <span class="sr-only">Go to first page</span>
                    <DoubleArrowLeftIcon class="h-4 w-4"/>
                </Button>
                <Button
                    variant ="outline"
                    class="h-8 w-8 p-0"
                >
                    <span class="sr-only">Go to previous page</span>
                    <ChevronLeftIcon class="h-4 w-4"/>
                </Button>
                <Button
                    variant ="outline"
                    class="h-8 w-8 p-0"
                >
                    <span class="sr-only">Go to next page</span>
                    <ChevronRightIcon class="h-4 w-4"/>
                </Button>
                <Button
                    variant ="outline"
                    class="hidden h-8 w-8 p-0 lg:flex"
                >
                    <span class="sr-only">Go to last page</span>
                    <DoubleArrowRightIcon class="h-4 w-4"/>
                </Button>
            </div>
        </div>
    </div>
</template>