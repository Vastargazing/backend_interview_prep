#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Скрипт для создания collapsible блоков кода в Markdown файле
"""

import re

def process_markdown_file(input_file, output_file):
    """Обрабатывает Markdown файл, делая блоки кода collapsible"""
    
    with open(input_file, 'r', encoding='utf-8') as f:
        lines = f.readlines()
    
    result = []
    i = 0
    
    while i < len(lines):
        line = lines[i].rstrip()
        
        # Если нашли блок кода Python
        if line == '```python':
            # Проверяем, не находимся ли уже в details блоке
            in_details = False
            for j in range(max(0, i-5), i):
                if '<details>' in lines[j]:
                    in_details = True
                    break
            
            if not in_details:
                # Добавляем collapsible блок
                result.append('<details>\n')
                result.append('<summary>💻 Код</summary>\n')
                result.append('\n')
            
            # Добавляем блок кода
            result.append(line + '\n')
            i += 1
            
            # Копируем содержимое до закрывающих ```
            while i < len(lines) and lines[i].rstrip() != '```':
                result.append(lines[i])
                i += 1
            
            # Добавляем закрывающий ```
            if i < len(lines):
                result.append(lines[i])
                i += 1
            
            if not in_details:
                # Закрываем details блок
                result.append('\n')
                result.append('</details>\n')
        else:
            result.append(lines[i])
            i += 1
    
    # Записываем результат
    with open(output_file, 'w', encoding='utf-8') as f:
        f.writelines(result)
    
    print(f"✅ Файл обработан: {output_file}")

if __name__ == "__main__":
    input_file = r"c:\Users\VA\Desktop\Backend Interview Questions 2025.md"
    output_file = r"c:\Users\VA\Desktop\Backend_Questions_Collapsible.md"
    
    process_markdown_file(input_file, output_file)
