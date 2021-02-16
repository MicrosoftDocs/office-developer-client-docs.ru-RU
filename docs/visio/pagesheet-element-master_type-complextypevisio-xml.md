---
title: Элемент PageSheet (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: Указывает свойства страницы рисования, связанной с хозяином.
ms.openlocfilehash: 94fde64b130c2a05c4bd70c97552fe4218171ce7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540618"
---
# <a name="pagesheet-element-master_type-complextype-visio-xml"></a>Элемент PageSheet (Master_Type complexType) (Visio XML)

Указывает свойства страницы рисования, связанной с хозяином.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Указывает хозяина в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |указывает ИД таблицы стилей, от которой необходимо наследовать форматирование заливки. Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ИД таблицы стилей, от которой необходимо наследовать форматирование строк. Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ИД таблицы стилей, от которой требуется наследовать форматирование текста. Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |необязательный  <br/> |Уникальный ИД элемента в родительском элементе.  <br/> |Значения типа xsd:string.  <br/> |
   

