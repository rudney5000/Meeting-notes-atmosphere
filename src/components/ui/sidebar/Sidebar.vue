<script setup lang="ts">

import { ref } from 'vue'
import { cn } from '@/lib/utils'
import { Button } from '@/components/ui/button'

import { Check, ChevronsUpDown } from 'lucide-vue-next'
import {
  Command,
  CommandEmpty,
  CommandGroup,
  CommandInput,
  CommandItem,
  CommandList
} from '@/components/ui/command'

import {
  Popover,
  PopoverContent,
  PopoverTrigger,
} from '@/components/ui/popover'

const reunions = [
  { value: 'next.js', label: 'Next.js' },
  { value: 'sveltekit', label: 'SvelteKit' },
  { value: 'nuxt.js', label: 'Nuxt.js' },
  { value: 'remix', label: 'Remix' },
  { value: 'astro', label: 'Astro' },
]

const open = ref(false)
const value = ref('')

</script>

<template>
    <div class="hidden sm:block sm:col-span-1 relative border-r border-gray-300 h-full">
        <div class="flex sm:bg-transparent p-2 sm:p-0 w-full">
            <div class="block relative w-full">
                <h2 class="mb-2 px-4 text-lg font-semibold tracking-tight">Cultes</h2>
                <div>
                    <Popover v-model:open="open">
                        <PopoverTrigger as-child>
                        <Button
                            variant="outline"
                            role="combobox"
                            :aria-expanded="open"
                            class="w-[200px] justify-between"
                        >
                            {{ value ? reunions.find((reunion) => reunion.value === value)?.label : 'Select reunion...' }}

                            <ChevronsUpDown class="ml-2 h-4 w-4 shrink-0 opacity-50" />
                        </Button>
                        </PopoverTrigger>
                        <PopoverContent class="w-[200px] p-0">
                        <Command v-model="value">
                            <CommandInput placeholder="Search framework..." />
                            <CommandEmpty>No reunion found.</CommandEmpty>
                            <CommandList>
                            <CommandGroup>
                                <CommandItem
                                v-for="reunion in reunions"
                                :key="reunion.value"
                                :value="reunion"
                                @select="open = false"
                                >
                                <Check
                                    :class="cn(
                                    'mr-2 h-4 w-4',
                                    value === reunion.value ? 'opacity-100' : 'opacity-0',
                                    )"
                                />
                                {{ reunion.label }}
                                </CommandItem>
                            </CommandGroup>
                            </CommandList>
                        </Command>
                        </PopoverContent>
                    </Popover>
                </div>
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