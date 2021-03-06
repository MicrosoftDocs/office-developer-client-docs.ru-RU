---
title: Структура потока FieldDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334897"
---
# <a name="fielddefinition-stream-structure"></a>Структура потока FieldDefinition

**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура потока FieldDefinition содержит либо определение поля определенного пользователем поля, либо набор параметров привязки данных для встроенного поля.
  
Можно программным образом управлять структурой потока FieldDefinition, если в структуре содержится определение поля определенного пользователем поля. Не следует пытаться программировать создание или изменение структуры FieldDefinition, если структура содержит параметры встроенного поля. Для поддержания таких параметров для встроенных полей необходимо использовать конструктор форм Microsoft Outlook microsoft.
  
> [!NOTE]
> Outlook поддерживает два формата определений полей: PropDefV1 и PropDefV2. Формат определений полей PropDefV1 содержит следующие элементы данных: Флаги, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI и ErrorANSI. Формат PropDefV2 содержит те же элементы и элементы InternalType и SkipBlocks. 
>
> Outlook не поддерживает версию Единого кода для элементов данных FormulaANSI, ValidationRuleANSI и ValidationTextANSI в формате определения поля PropDefV2. Если эти элементы содержат символы, не содержащие ASCII, эти символы могут быть интерпретируются непоследовательно в зависимости от страницы кода ANSI компьютера, на котором Outlook запущен. Поэтому для этих элементов данных следует использовать только значения строк, состоящие полностью из символов ASCII. 
  
Элементы данных в этом потоке хранятся в порядке маленького byte, немедленно следуя друг за другом в порядке, указанном ниже.
  
- Флаги: DWORD (4 bytes), сочетание нулей или нескольких флагов, значения и значения которых перечислены в следующей таблице.
    
    |**Имя флага**|**Значение**|**Описание**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |Структура FieldDefinition содержит определение пользовательского поля.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Для управления формами, связанного с этим полем, для этого поля требуется поле для значения **A,** выбранное на вкладке **Проверка** диалогового окна **Свойства.**  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Для управления формами, связанного с  этим полем, в диалоговом окне Свойства  выбирается поле Включить это поле для печати и сохранить Как.   <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Для управления формами, связанного с  этим полем, в диалоговом окне Свойства автоматически выбирается поле Calculate этой формулы.    <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Это поле комбинации  типов, в  диалоговом окне "Сочетание Формулы поля" и любые текстовые фрагменты друг с другом, выбранные в диалоговом окне **Combination Formula Field.**  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Это поле имеет тип Combination **и** имеет только первое не пустое поле, игнорируя последующие **параметры,** выбранные в диалоговом окне **Сочетание формулы** поля.  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Этот флаг не используется Outlook, но он включен для всех определений полей, определенных пользователем.  <br/> |
   
- VT: WORD (2 байта), тип данных поля, который является константой из [перемерения VARENUM.](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) 
    
- DispId: DWORD (4 bytes), идентификатор отправки поля. Для поля, определяемого пользователем, значение 0.
    
- NmidNameLength: WORD (2 bytes), количество элементов в массиве NmidName.
    
- NmidName: массив WCHAR. Для определения поля, определяемого пользователем, это представление имени поля Unicode (UTF-16). Количество этого массива равно NmidNameLength.
    
- NameANSI: структура [потока PackedAnsiString.](packedansistring-stream-structure.md) Это представление ANSI имени поля. 
    
- FormulaANSI: структура потока PackedAnsiString. Это представление ANSI формулы вычислений для поля. Оно отображается в разделе **Начальное** значение вкладки **Значение** диалоговое **окно Свойства** управления формами, связанного с этим полем. 
    
- ValidationRuleANSI: структура потока PackedAnsiString. Это представление ANSI формулы проверки поля. Оно отображается в текстовом окне Формула проверки на вкладке **Проверка** диалогового **окна Свойства,** связанного с этим полем.  
    
- ValidationTextANSI: структура потока PackedAnsiString. Это представление ANSI текста сбоя проверки поля. Оно отображается в текстовом окне Для отображения этого  сообщения, если проверка не удается на вкладке Проверка диалогового окна **Свойства,** связанного с этим полем управления формами.  
    
- ErrorANSI: структура потока PackedAnsiString. Outlook не использует этот элемент; этот элемент следует настроить на пустую строку.
    
- InternalType: DWORD (4 bytes), внутренний тип поля. Этот элемент данных присутствует только в том случае, если формат определения поля является PropDefV2. Внутренний тип — это одно из следующих значений, каждое из которых соответствует типу в диалоговом окне **New Field** для определенных пользователем полей. 
    
    |**Имя внутреннего типа**|**Значение**|**Соответствующий тип в **диалоговом** окне New Field**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Number** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |Денежный  <br/> |3  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4   <br/> |**Да или нет** <br/> |
    |iTypeDateTime  <br/> |5   <br/> |**Дата/время** <br/> |
    |iTypeDuration  <br/> |6   <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7   <br/> |**Сочетание**, с **отображением только** первого непустого поля, игнорируя последующие параметры, выбранные в диалоговом окне **Сочетание формулы** поля.  <br/> |
    |iTypeFormula  <br/> |8   <br/> |**Формула** <br/> |
    |iTypeResult  <br/> |9   <br/> |Этот тип не используется для определенных пользователем полей.  <br/> |
    |iTypeVariant  <br/> |10   <br/> |Этот тип не используется для определенных пользователем полей.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Этот тип не используется для определенных пользователем полей.  <br/> |
    |iTypeConcat  <br/> |12   <br/> |**Сочетание** с **полями Присоединение** и любыми текстовыми фрагментами друг с другом параметром, выбранным в диалоговом окне **Сочетание формулы** поля.  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Ключевое слово** <br/> |
    |iTypeInteger  <br/> |14   <br/> |**Integer** <br/> |
   
- SkipBlocks: серия из одной или более структур [потока SkipBlock.](skipblock-stream-structure.md) Этот элемент данных присутствует только в том случае, если формат определения поля является PropDefV2. Если формат определения поля является PropDefV2, серия должна содержать по крайней мере одну структуру SkipBlock, структуру SkipBlock, которая имеет элемент данных Size, равный 0, и серия должна начинаться и заканчиваться с помощью этой структуры SkipBlock. 
    
   Назначение структуры SkipBlock зависит от ее относительного положения в серии SkipBlocks. Если определение поля находится в формате PropDefV2, а первая структура не является структурой прекращения (элемент данных Size больше 0), Outlook предполагает, что первая структура SkipBlock указывает имя поля в Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Если первый SkipBlock — это завершаемая структура, для определения имени поля используется элемент данных NameANSI. Если эта строка содержит какие-либо символы, не относимые к ASCII, эти символы могут быть интерпретируются непоследовательно в зависимости от страницы кода ANSI компьютера, на котором Outlook запущен. Чтобы предотвратить такие несоответствия, обязательно укажите первый SkipBlock в создаваемом определении поля, по крайней мере, если имя поля включает символы, не относимые к ASCII. 
  
   Если в будущей версии формата определения полей будут вводиться дополнительные фрагменты данных в потоке FieldDefinition, эти данные можно хранить в виде дополнительных структур потока SkipBlock в серии SkipBlocks перед прекращением структуры SkipBlock, которая имеет элемент данных Size, равный 0. Более ранние версии Outlook могут безопасно игнорировать эти дополнительные структуры SkipBlock до завершаемой структуры SkipBlock и по-прежнему правильно обрабатывать все поддерживаемые ими блоки.
    
## <a name="see-also"></a>См. также

- [Outlook Элементы и поля](outlook-items-and-fields.md)
- [Структуры потока](stream-structures.md)
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)

