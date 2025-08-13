---
title: Frequently Asked Questions
subtitle:  Answers to frequently asked questions about the Quantum Challenge 2025
menu_title: FAQ
menu_icon: question-circle
---

{% include subpage_header.html %}

<!-- Include the Tailwind 4 elements script -->
<script src="https://cdn.jsdelivr.net/npm/@tailwindplus/elements@1" type="module"></script>

<section class="px-5 max-w-screen-lg mx-auto text-white py-10 gap-4 flex flex-col">
  <div class="mx-auto max-w-4xl">
  

    {% for section in site.faq_sections %}
      <h3 class="text-2xl font-semibold text-white mb-6 mt-12">{{ section.title }}</h3>
      
      <div class="space-y-4 prose">
        {% for faq in section.questions %}
          <div class="border border-electron/25 rounded-lg">
            
              <button type="button" command="--toggle" commandfor="faq-{{ section.id }}-{{ forloop.index }}" class="flex w-full items-start justify-between text-left text-white p-4 hover:bg-electron/5 transition-colors duration-200 cursor-pointer">
                <span class="text-base font-space-mono pr-4">{{ faq.question }}</span>
                <span class="ml-6 flex h-7 items-center flex-shrink-0">
                  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" data-slot="icon" aria-hidden="true" class="size-6 in-aria-expanded:hidden">
                    <path d="M12 6v12m6-6H6" stroke-linecap="round" stroke-linejoin="round" />
                  </svg>
                  <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" data-slot="icon" aria-hidden="true" class="size-6 not-in-aria-expanded:hidden">
                    <path d="M18 12H6" stroke-linecap="round" stroke-linejoin="round" />
                  </svg>
                </span> 
              </button>
            
            <el-disclosure id="faq-{{ section.id }}-{{ forloop.index }}" hidden class="contents">
              <dd class="px-4 pb-4">
                <div class="text-base text-white">
                  {{ faq.answer | markdownify }}
                </div>
              </dd>
            </el-disclosure>
          </div>
        {% endfor %}
      </div>
    {% endfor %}

  </div>
</section>