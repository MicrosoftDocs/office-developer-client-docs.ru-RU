---
title: Элемент connects (Пажеконтентс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Содержит элемент Connect для каждого подключения между двумя фигурами в документе.
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538713"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a>Элемент connects (Пажеконтентс_типе complexType) (XML для Visio)

Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Коннектс_типе](connects_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |страница #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Мастерконтентс](mastercontents-elementvisio-xml.md) <br/> |[Пажеконтентс_типе](pagecontents_type-complextypevisio-xml.md) <br/> |Задает сведения о фигурах на главной странице или странице документа в документе.  <br/> |
|[Пажеконтентс](pagecontents-elementvisio-xml.md) <br/> |[Пажеконтентс_типе](pagecontents_type-complextypevisio-xml.md) <br/> |Задает сведения о фигурах на главной странице или странице документа в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Connect](connect-element-connects_type-complextypevisio-xml.md) <br/> |[Коннект_типе](connect_type-complextypevisio-xml.md) <br/> |Представляет соединение между двумя фигурами в документе, например линии и поле на организационной диаграмме.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

