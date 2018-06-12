---
title: Элемент окна (Windows_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Представляет окно в экземпляре Microsoft Visio. Этот элемент содержит сведения, необходимые для точно повторного создания окна интерфейса пользователя в рабочей области приложения при первом открытии файла в Visio.
ms.openlocfilehash: 762b689d625c7865696a0bf8bb8c4acc25e3d8eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815172"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Элемент окна (Windows_Type complexType) ('Visio XML»)

Представляет окно в экземпляре Microsoft Visio. Этот элемент содержит сведения, необходимые для точно повторного создания окна интерфейса пользователя в рабочей области приложения при первом открытии файла в Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Windows.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Содержит элементы **окна** документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Указывает, включена ли функция динамической таблицы для документа или окна.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Определяет объекты, которые связывания фигуры на при включении связывающих в документе.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли в окне точек подключения.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Указывает, отображается ли сетки в окне документа.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли руководства в окне документа.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли разрывов страниц в окне.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Указывает, отображаются ли линейки в окне документа.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Указывает, будет ли параметр расширения с определенным оснастке включена или отключена для активного окна.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Определяет объекты, которые привязать фигуры при привязка активна в окне.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Указывает группу windows объединенные набор элементов, членом которых является окна.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Содержит целое число, указывающее относительное положение набор элементов в группе, в окне.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Задает ширину вкладки окно рисунка (как часть общая ширина окна документа).  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Контейнер  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор контейнера: страница, отчет или образец. Только соответствующие и требуется, если указан **ContainerType** .  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |XSD:Token  <br/> |необязательный  <br/> |Может быть одно из следующих значений: документа, страницы или образец. Соответствующие только при **WindowType** указан как документа или листа.  <br/> |Значения типа xsd:token.  <br/> |
|Документ  <br/> |XSD:String  <br/> |необязательный  <br/> |Путь к файлу документа, отображаемые в это окно.  <br/> |Значения типа xsd:string.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Образец  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Основной идентификатор, если это окно отображается главный.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Page  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор страницы, если это окно отображается страница. Соответствующие, только если **WindowType** задано документа и **ContainerType** указано как страницы.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор окна, в котором содержится это окно набор элементов. Соответствующие только в том случае, если указано **WindowType** как набор элементов.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Только для чтения флаг, если этот набор элементов не элементов документа.  <br/> |Значения типа xsd:boolean.  <br/> |
|Лист  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор листа в контейнере. Соответствующие только в том случае, если контейнер указано на листе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD: double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** укажите центральной точки на странице, новое представление (окно) предполагается, что при его открытии.  <br/> |Значения типа XSD: double.  <br/> |
|ViewCenterY  <br/> |XSD: double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** укажите центральной точки на странице, новое представление (окно) предполагается, что при его открытии.  <br/> |Значения типа XSD: double.  <br/> |
|ViewScale  <br/> |XSD: double  <br/> |необязательный  <br/> |Масштаб по умолчанию для использования при открытии нового представления (окно) страницы. Например 1 = 100%. 1,5 = 150% и т. д.  <br/> |Значения типа XSD: double.  <br/> |
|WindowHeight  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Высота окна прямоугольника.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |XSD:Short  <br/> |необязательный  <br/> |Левая координата прямоугольника окна.  <br/> |Значения типа xsd:short.  <br/> |
|WindowState  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указание целое число двоичных флагов.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |XSD:Short  <br/> |необязательный  <br/> |Верхняя координата прямоугольника окна.  <br/> |Значения типа xsd:short.  <br/> |
|WindowType  <br/> |XSD:Token  <br/> |Обязательный  <br/> |Значение перечисления, может иметь одно из следующих значений: документа, листа, набор элементов или значок.  <br/> |Значения типа xsd:token.  <br/> |
|WindowWidth  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Ширина прямоугольника окна.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

