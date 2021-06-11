---
title: Элемент PageSheet (Page_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Указывает свойства страницы рисования, связанные со страницей рисования.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540625"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a>Элемент PageSheet (Page_Type ComplexType) (Visio XML)

Указывает свойства страницы рисования, связанные со страницей рисования.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |pages.xml  <br/> |
   
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
|[Page](page-element-pages_type-complextypevisio-xml.md) <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие страницу в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ID листа стилей, из которого можно наследовать форматирование заполнения. Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ID листа стилей, из которого можно наследовать форматирование строки. Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ID листа стилей, из которого можно наследовать форматирование текста. Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |необязательный  <br/> |Уникальный ID элемента в родительском элементе.  <br/> |Значения типа xsd:string.  <br/> |
   

