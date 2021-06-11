---
title: Элемент MasterShortcut (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 62f0e093-5385-e552-f91a-02a65eb0e6e1
description: Указывает мастер-ярлык, определенный в документе.
ms.openlocfilehash: 94ac64ff0080bf7d50df67674022ce53f32339a4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538209"
---
# <a name="mastershortcut-element-masters_type-complextype-visio-xml"></a>Элемент MasterShortcut (Masters_Type complexType) (Visio XML)

Указывает мастер-ярлык, определенный в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[MasterShortcut_Type](mastershortcut_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |master#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="MasterShortcut" type="MasterShortcut_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Содержит **основные** элементы документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Icon](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Указывает кодированный двоичный значок MIME (Multipurpose Internet Mail Extensions) (в формате .ico) для элемента **Master** или **MasterShortcut** в документе.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Указывает, выравнивается ли текст элемента в окне трафарета слева, справа или в центре.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Размер значка элемента.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ID элемента в родительском элементе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Определяет, ведет ли мастер себя как настраиваемый шаблон.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd:string  <br/> |необязательный  <br/> |Подсказка панели состояния и подсказки инструмента для элемента.  <br/> |Значения типа xsd:string.  <br/> |
|ShortcutHelp  <br/> |xsd:string  <br/> |необязательный  <br/> |Строка справки для элемента.  <br/> |Значения типа xsd:string.  <br/> |
|ShortcutURL  <br/> |xsd:string  <br/> |необязательный  <br/> |URL-адрес элемента **MasterShortcut.**  <br/> |Значения типа xsd:string.  <br/> |
   

