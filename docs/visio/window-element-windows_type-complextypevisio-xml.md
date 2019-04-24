---
title: Элемент Window (Виндовс_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Представляет открытое окно в экземпляре Microsoft Visio. Этот элемент содержит сведения, необходимые для точного повторного создания окна пользовательского интерфейса в рабочей области приложения при первом открытии файла в Visio.
ms.openlocfilehash: 676818ddea7747a17b0fe296da515e80c4ffd98f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339902"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Элемент Window (Виндовс_типе complexType) (' XML ' Visio ')

Представляет открытое окно в экземпляре Microsoft Visio. Этот элемент содержит сведения, необходимые для точного повторного создания окна пользовательского интерфейса в рабочей области приложения при первом открытии файла в Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Windows. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Виндовс_типе](windows_type-complextypevisio-xml.md) <br/> |Содержит элементы **окна** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[Динамикгриденаблед_типе](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Указывает, включена ли динамическая сетка для документа или окна.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[Глуесеттингс_типе](gluesettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, на которые фигуры привязываются при включении параметра приклеивание в документе.  <br/> |
|[Шовконнектионпоинтс](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[Шовконнектионпоинтс_типе](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли точки подключения в окне.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[Шовгрид_типе](showgrid_type-complextypevisio-xml.md) <br/> |Указывает, отображается ли сетка в окне документа.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[Шовгуидес_типе](showguides_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли направляющие в окне документа.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[Шовпажебреакс_типе](showpagebreaks_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли разрывы страниц в окне.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[Шоврулерс_типе](showrulers_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли линейки в окне документа.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[Снапанглес_типе](snapangles_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **снапангле** .  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[Снапекстенсионс_типе](snapextensions_type-complextypevisio-xml.md) <br/> |Указывает, включен или отключен указанный параметр расширения привязки для активного окна.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[Снапсеттингс_типе](snapsettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, к которым привязываются фигуры при активации привязки в окне.  <br/> |
|[СтенЦилграуп](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[СтенЦилграуп_типе](stencilgroup_type-complextypevisio-xml.md) <br/> |Задает группу Объединенных окон набора элементов, членом которой является окно.  <br/> |
|[СтенЦилграуппос](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[СтенЦилграуппос_типе](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Содержит целое число, задающее относительное положение набора элементов в группе в окне.  <br/> |
|[Табсплиттерпос](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[Табсплиттерпос_типе](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Задает ширину элемента управления "вкладка страницы" в окне документа (в виде доли общей ширины окна документа).  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор контейнера: страница, лист или образец. Уместно и обязательно, если указан **контаинертипе** .  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|ContainerType  <br/> |XSD: маркер  <br/> |необязательный  <br/> |Может принимать одно из следующих значений: Document, Page или Master. Применяется только в том случае, если для **виндовтипе** задано значение "документ" или "лист".  <br/> |Значения типа маркера XSD:.  <br/> |
|Document  <br/> |XSD: строка  <br/> |необязательный  <br/> |Путь к файлу документа, отображаемого в этом окне.  <br/> |Значения типа String: XSD.  <br/> |
|ИД  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в родительском элементе.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Master  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Основной идентификатор, если в этом окне отображается образец.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Page  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор страницы, если в этом окне отображается страница. Уместно, только если для **виндовтипе** задано значение Drawing, а **контаинертипе** задано как Page.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|ParentWindow  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |ИДЕНТИФИКАТОР окна, в котором находится данное окно набора элементов. Уместно, только если **виндовтипе** указан как набор элементов.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|ReadOnly  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Флаг только для чтения, если этот набор не является трафаретом документа.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Таблица  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор листа в контейнере. Уместно, только если в качестве контейнера указан лист.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Виевцентеркс  <br/> |XSD: Double  <br/> |необязательный  <br/> |**Виевцентеркс** и **виевцентери** указывают центральную точку на странице, которая предполагается при открытии нового представления (окна).  <br/> |Значения типа XSD: Double.  <br/> |
|Виевцентери  <br/> |XSD: Double  <br/> |необязательный  <br/> |**Виевцентеркс** и **виевцентери** указывают центральную точку на странице, которая предполагается при открытии нового представления (окна).  <br/> |Значения типа XSD: Double.  <br/> |
|Виевскале  <br/> |XSD: Double  <br/> |необязательный  <br/> |Фактор увеличения по умолчанию, используемый при открытии нового представления (окна) страницы. Например, 1 = 100%; 1,5 = 150% и т. д.  <br/> |Значения типа XSD: Double.  <br/> |
|WindowHeight  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Высота прямоугольника окна.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|WindowLeft  <br/> |XSD: Short  <br/> |необязательный  <br/> |Левая координата прямоугольника окна.  <br/> |Значения типа XSD: Short.  <br/> |
|WindowState  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Целое число, задающее битовые флаги.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|WindowTop  <br/> |XSD: Short  <br/> |необязательный  <br/> |Верхняя координата прямоугольника окна.  <br/> |Значения типа XSD: Short.  <br/> |
|Виндовтипе  <br/> |XSD: маркер  <br/> |Обязательный  <br/> |Перечислимое значение, которое может быть одним из следующих: рисунок, лист, трафарет или значок.  <br/> |Значения типа маркера XSD:.  <br/> |
|WindowWidth  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Ширина прямоугольника окна.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

