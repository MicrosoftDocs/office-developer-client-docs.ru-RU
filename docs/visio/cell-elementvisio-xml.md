---
title: Элемент Cell (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3131bfbb-9bf6-d15d-c6ca-2f15bd038f39
description: Указывает элементы ячейки, которые могут содержаться в таблицах DocumentSheet, StyleSheet, PageSheet или ShapeSheet.
ms.openlocfilehash: 2b76abeb83fb7251bf492e92d8dd1a81feeab092
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542312"
---
# <a name="cell-element-visio-xml"></a>Элемент Cell (Visio XML)

Указывает элементы ячейки, которые могут содержаться в таблицах DocumentSheet, StyleSheet, PageSheet или ShapeSheet.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml, pages.xml, masters.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Указывает элементы ячейки, которые предоставляют сведения для определения фигуры.  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Определяет структуру таблицы документов.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Представляет стиль, определенный в документе.  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы рисования, связанной с хозяином.  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Указывает свойства страницы рисования, связанной со страницей рисования.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Указывает ссылку на страницу рисования.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |необязательный  <br/> |Указывает, что формула оценивается как ошибка. Значение E **—** текущее значение (строка сообщения об ошибке); Значение атрибута **V** является последним допустимым значением.  <br/> |Строка сообщения об ошибке.  <br/> |
|F  <br/> |xsd:string  <br/> |необязательный  <br/> | Представляет формулу элемента. Этот атрибут может содержать одну из следующих строк:  <br/>  '(some formula)', если формула существует локально  <br/>  `No Formula` если формула удалена или заблокирована локально  <br/>  `Inh` если формула унаследована.  <br/> |Формула.  <br/> |
|N  <br/> |xsd:string  <br/> |Обязательный  <br/> |Представляет имя ячейки **ShapeSheet.**  <br/> |Имя ячейки **ShapeSheet.**  <br/> См. раздел "Замечания" ниже.  <br/> |
|U  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет единицу измерения, значение по умолчанию — DL.  <br/> |Единицы ячейки.  <br/> |
|V  <br/> |xsd:string  <br/> |необязательный  <br/> |Представляет значение ячейки.  <br/> |Значение ячейки **ShapeSheet.**  <br/> |
   
## <a name="remarks"></a>Примечания

Атрибут **N** этого элемента **Cell** должен быть одним из ограниченного набора значений, соответствующих ячейкам ShapeSheet. Чтобы определить значения атрибута **N,** допустимого для этого элемента Cell, обратитесь к таблице **ниже.** 
  
|**Значение**|**Описание**|**Дополнительные сведения**|
|:-----|:-----|:-----|
|AddMarkup  <br/> |Указывает, просматривается ли документ на разметку.  <br/> |[AddMarkup Cell (Document Properties Section)](addmarkup-cell-document-properties-section.md) <br/> |
|AlignBottom  <br/> |Определяет вертикальное положение (относительно начала родительского) горизонтального руководства или точки направляния, к которой выравнивается нижняя граница фигуры.  <br/> |[AlignBottom Cell (Alignment Section)](alignbottom-cell-alignment-section.md) <br/> |
|AlignCenter  <br/> |Определяет горизонтальное положение по отношению к источнику родительского вертикального руководства или точки направляния, к которой выравнивается горизонтальный центр фигуры.  <br/> |[AlignCenter Cell (Alignment Section)](aligncenter-cell-alignment-section.md) <br/> |
|AlignLeft  <br/> |Определяет горизонтальное положение относительно начала родительского вертикального руководства или точки направляния, к которой выравнивается левая граница фигуры.  <br/> |[AlignLeft Cell (Alignment Section)](alignleft-cell-alignment-section.md) <br/> |
|AlignMiddle  <br/> |Определяет вертикальное положение (относительно начала родительского) горизонтального руководства или точки направляния, к которой выравнивается центр вертикальной фигуры.  <br/> |[AlignMiddle Cell (Alignment Section)](alignmiddle-cell-alignment-section.md) <br/> |
|AlignRight  <br/> |Определяет горизонтальное положение относительно начала родительского вертикального руководства или точки направляния, к которой выровнена правая граница фигуры.  <br/> |[AlignRight Cell (Alignment Section)](alignright-cell-alignment-section.md) <br/> |
|AlignTop  <br/> |Определяет вертикальное положение горизонтального руководства или точки направляния, с которым выровнена верхняя граница фигуры относительно начала родительского начала.  <br/> |[AlignTop Cell (Alignment Section)](aligntop-cell-alignment-section.md) <br/> |
|Угловая  <br/> |Представляет текущий угол поворота фигуры относительно родительского. Формула по умолчанию для определения угла поворота 1-D фигуры: =ATAN2(EndY-BeginY,EndX-BeginX).  <br/> |[Angle Cell (Shape Transform Section)](angle-cell-shape-transform-section.md) <br/> |
|AvenueSizeX  <br/> |Определяет объем горизонтального пространства между фигурами на странице рисования при разметке фигур в диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout", а затем щелкните "Дополнительные параметры макета").  <br/> |[AvenueSizeX Cell (Page Layout Section)](avenuesizex-cell-page-layout-section.md) <br/> |
|AvenueSizeY  <br/> |Определяет объем вертикального пространства между фигурами на странице рисования при разметке фигур в диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout", а затем щелкните "Дополнительные параметры макета"). Определяет объем вертикального пространства между фигурами на странице рисования при разметке фигур в диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout", а затем щелкните "Дополнительные параметры макета").  <br/> |[AvenueSizeY Cell (Page Layout Section)](avenuesizey-cell-page-layout-section.md) <br/> |
|AvoidPageBreaks  <br/> |Определяет, можно ли размещать фигуры на разрывы страниц, когда фигуры выровнены пошагово, добавочно или и то, и другое.  <br/> |[AvoidPageBreaks Cell (Page Layout Section)](avoidpagebreaks-cell-page-layout-section.md) <br/> |
|BeginArrow  <br/> |Указывает, имеет ли строка стрелку или другой формат конца линии на первой вершине. Введите число от 0 до 45 или функцию USE с именем пользовательского конца строки или используйте диалоговое окно "Строка".  <br/> |[BeginArrow Cell (Line Format Section)](beginarrow-cell-line-format-section.md) <br/> |
|BeginArrowSize  <br/> |Определяет размер наконечник в начале строки.  <br/> |[BeginArrowSize Cell (Line Format Section)](beginarrowsize-cell-line-format-section.md) <br/> |
|BeginX  <br/> |Представляет x-координату точки начала 1-D фигуры относительно начала родительской фигуры. Представляет x-координату точки начала 1-D фигуры относительно начала родительской фигуры.  <br/> |[BeginX Cell (1-D Endpoints Section)](beginx-cell-1-d-endpoints-section.md) <br/> |
|BeginY  <br/> |Представляет координату y точки начала 1-D фигуры относительно начала родительской фигуры.  <br/> |[BeginY Cell (1-D Endpoints Section)](beginy-cell-1-d-endpoints-section.md) <br/> |
|BegTrigger  <br/> |Содержит формулу триггера, созданную приложением, которая определяет, следует ли перемещать точки начала одно d фигуры для поддержания соединения с другой фигурой.  <br/> |[BegTrigger Cell (Glue Info Section)](begtrigger-cell-glue-info-section.md) <br/> |
|BevelBottomHeight  <br/> |Определяет высоту нижней волны фигуры в точках.  <br/> |[BevelBottomHeight Cell (Bevel Properties Section)](bevelbottomheight-cell-bevel-properties-section.md) <br/> |
|BevelBottomType  <br/> |Указывает нижний тип огона фигуры.  <br/> |[BevelBottomType Cell (Bevel Properties Section)](bevelbottomtype-cell-bevel-properties-section.md) <br/> |
|BevelBottomWidth  <br/> |Определяет ширину нижней области в точках.  <br/> |[BevelBottomWidth Cell (Bevel Properties Section)](bevelbottomwidth-cell-bevel-properties-section.md) <br/> |
|BevelContourColor  <br/> |Определяет цвет контура bevel в RGB-значении или в значении, определяемом активной темой.  <br/> |[BevelContourColor Cell (Bevel Properties Section)](bevelcontourcolor-cell-bevel-properties-section.md) <br/> |
|BevelContourSize  <br/> |Определяет размер контура bevel в точках.  <br/> |[BevelContourSize Cell (Bevel Properties Section)](bevelcontoursize-cell-bevel-properties-section.md) <br/> |
|BevelDepthColor  <br/> |Определяет цвет глубины ленты в качестве значения RGB или в качестве значения активной темы.  <br/> |[BevelDepthColor Cell (Bevel Properties Section)](beveldepthcolor-cell-bevel-properties-section.md) <br/> |
|BevelDepthSize  <br/> |Определяет размер глубины ленты в точках.  <br/> |[BevelDepthSize Cell (Bevel Properties Section)](beveldepthsize-cell-bevel-properties-section.md) <br/> |
|BevelLightingAngle  <br/> |Определяет угол вспышки по отношению к градусам.  <br/> |[BevelLightingAngle Cell (Bevel Properties Section)](bevellightingangle-cell-bevel-properties-section.md) <br/> |
|BevelLightingType  <br/> |Определяет тип освещения, используемого эффектом bevel.  <br/> |[BevelLightingType Cell (Bevel Properties Section)](bevellightingtype-cell-bevel-properties-section.md) <br/> |
|BevelMaterialType  <br/> |Определяет тип материала, из которого состоит bevel.  <br/> |[BevelMaterialType Cell (Bevel Properties Section)](bevelmaterialtype-cell-bevel-properties-section.md) <br/> |
|BevelTopHeight  <br/> |Определяет высоту верхнего верха фигуры в точках.  <br/> |[BevelTopHeight Cell (Bevel Properties Section)](beveltopheight-cell-bevel-properties-section.md) <br/> |
|BevelTopType  <br/> |Определяет тип верхней границы фигуры.  <br/> |[BevelTopType Cell (Bevel Properties Section)](beveltoptype-cell-bevel-properties-section.md) <br/> |
|BevelTopWidth  <br/> |Определяет ширину верхней полосы в точках.  <br/> |[BevelTopWidth Cell (Bevel Properties Section)](beveltopwidth-cell-bevel-properties-section.md) <br/> |
|BlockSizeX  <br/> |Определяет размер горизонтального блока, область, в которой каждая из фигур должна умещаться на странице рисования при отрисовке фигур с помощью диалоговых окна "Настройка макета".  <br/> |[BlockSizeX Cell (Page Layout Section)](blocksizex-cell-page-layout-section.md) <br/> |
|BlockSizeY  <br/> |Определяет размер вертикального блока , область, в которой каждая из фигур должна умещаться на странице рисования при отрисовке фигур с помощью диалоговое окно "Настройка макета".  <br/> |[BlockSizeY Cell (Page Layout Section)](blocksizey-cell-page-layout-section.md) <br/> |
|Размытие  <br/> |Размытие или размягка толчайного изображения. Значение по умолчанию — 0%.  <br/> |[Blur Cell (Image Properties Section)](blur-cell-image-properties-section.md) <br/> |
|BottomMargin  <br/> |Определяет расстояние между нижней границей текстового блока и последней строкой текста в нем.  <br/> |[BottomMargin Cell (Text Block Format Section)](bottommargin-cell-text-block-format-section.md) <br/> |
|Яркость  <br/> |Настраивает яркость толщины толщины изображения.  <br/> |[Brightness Cell (Image Properties Section](brightness-cell-image-properties-section.md) <br/> |
|Календарь  <br/> |Определяет календарь, который используется, когда формула ячейки содержит сведения о дате.  <br/> |[Calendar Cell (Miscellaneous Section)](calendar-cell-miscellaneous-section.md) <br/> |
|Календарь  <br/> |Определяет календарь, используемый для данных фигуры, когда типом данных является Date.  <br/> |[Calendar Cell (Shape Data Section)](calendar-cell-shape-data-section.md) <br/> |
|Календарь  <br/> |Определяет календарь, используемый для текстового поля, когда типом данных является Date.  <br/> |[Calendar Cell (Text Fields Section)](calendar-cell-text-fields-section.md) <br/> |
|CenterX  <br/> |Определяет, находится ли страница рисования по горизонтали на странице принтера.  <br/> |[CenterX Cell (Print Properties Section)](centerx-cell-print-properties-section.md) <br/> |
|CenterY  <br/> |Определяет, находится ли страница рисования по центру вертикально на странице принтера.  <br/> |[CenterY Cell (Print Properties Section)](centery-cell-print-properties-section.md) <br/> |
|ClippingPath  <br/> |Содержит ссылку на геометрию пути, к которую привязано изображение.  <br/> |[ClippingPath Cell (Foreign Image Info Section)](clippingpath-cell-foreign-image-info-section.md) <br/> |
|ColorSchemeIndex  <br/> |Определяет цветовую схему темы, применяемой к фигуре, в виде integer.  <br/> |[ColorSchemeIndex Cell (Theme Properties Section)](colorschemeindex-cell-theme-properties-section.md) <br/> |
|Примечание  <br/> |Содержит текст, который отображается в комментарии.  <br/> |[Comment Cell (Annotation Section)](comment-cell-annotation-section.md) <br/> |
|Примечание  <br/> |Содержит текст комментария в строковом формате для фигуры.  <br/> |[Comment Cell (Miscellaneous Section)](comment-cell-miscellaneous-section.md) <br/> |
|CompoundType  <br/> |Определяет составной тип линии фигуры.  <br/> |[CompoundType Cell (Line Format Section)](compoundtype-cell-line-format-section.md) <br/> |
|ConFixedCode  <br/> |Определяет, когда соединителю необходимо перенаупределять.  <br/> |[ConFixedCode Cell (Shape Layout Section)](confixedcode-cell-shape-layout-section.md) <br/> |
|ConLineJumpCode  <br/> |Определяет, когда соединители переходов.  <br/> |[ConLineJumpCode Cell (Shape Layout Section)](conlinejumpcode-cell-shape-layout-section.md) <br/> |
|ConLineJumpDirX  <br/> |Определяет направление перехода по строке для переходов по горизонтали для фигуры.  <br/> |[ConLineJumpDirX Cell (Shape Layout Section)](conlinejumpdirx-cell-shape-layout-section.md) <br/> |
|ConLineJumpDiry  <br/> |Определяет направление перехода по строке для переходов по линии, происходящих на вертикальном динамическом соединители для фигуры.  <br/> |[ConLineJumpDirY Cell (Shape Layout Section)](conlinejumpdiry-cell-shape-layout-section.md) <br/> |
|ConLineJumpStyle  <br/> |Определяет стиль перехода по строкам для динамического соединитела.  <br/> |[ConLineJumpStyle Cell (Shape Layout Section)](conlinejumpstyle-cell-shape-layout-section.md) <br/> |
|ConLineRouteExt  <br/> |Определяет внешний вид соединители.  <br/> |[ConLineRouteExt Cell (Shape Layout Section)](conlinerouteext-cell-shape-layout-section.md) <br/> |
|ConnectorSchemeIndex  <br/> |Определяет схему соединители темы, применяемой к фигуре, в виде integer.  <br/> |[ConnectorSchemeIndex Cell (Theme Properties Section)](connectorschemeindex-cell-theme-properties-section.md) <br/> |
|Контраст  <br/> |Настраивает контрастность ток-изображения.  <br/> |[Contrast Cell (Image Properties Section)](contrast-cell-image-properties-section.md) <br/> |
|Авторское право  <br/> |Содержит строку, представляющую понятное для человека заявление об авторских правах  <br/> ||
|CtrlAsInput  <br/> |Определяет, какая фигура является родительской при использовании фигур с окнами управления. Эта ячейка задает поведение для всех фигур на странице рисования.  <br/> |[CtrlAsInput Cell (Page Layout Section)](ctrlasinput-cell-page-layout-section.md) <br/> |
|DefaultTabStop  <br/> |Определяет интервал остановки вкладки по умолчанию в текстовом блоке.  <br/> |[DefaultTabstop Cell (Text Block Format Section)](defaulttabstop-cell-text-block-format-section.md) <br/> |
|Denoise  <br/> |Удаляет шум (пиксели с случайно распределенными уровнями цвета) из точеченого изображения.  <br/> |[Denoise Cell (Image Properties Section)](denoise-cell-image-properties-section.md) <br/> |
|DisplayLevel  <br/> |Определяет полосу уровня отображения (относительный диапазон группировки Z-порядка) для фигуры.  <br/> |[DisplayLevel Cell (Shape Layout Section)](displaylevel-cell-shape-layout-section.md) <br/> |
|DisplayMode  <br/> |Определяет, как отображается фигура группы и ее члены.  <br/> |[DisplayMode Cell (Group Properties Section)](displaymode-cell-group-properties-section.md) <br/> |
|DisplayMode  <br/> |Определяет, отображается ли тег действия, когда пользователь нанося указатель на тег, когда фигура выбрана, или все время.  <br/> |[DisplayMode Cell (Smart Tags Section)](displaymode-cell-action-tags-section.md) <br/> |
|DistanceFromGround  <br/> |Определяет расстояние, на которое объект вызывается от нуля в точках при повороте в 3-D.  <br/> |[DistanceFromGround Cell (3-D Rotation Properties)](distancefromground-cell-3-d-rotation-properties.md) <br/> |
|DocLangID  <br/> |Указывает язык по умолчанию для документа.  <br/> |[DocLangID Cell (Document Properties Section)](doclangid-cell-document-properties-section.md) <br/> |
|DocLockDuplicatePage  <br/> |Определяет, можно ли дублировать страницы в документе в качестве boolean.  <br/> |[DocLockDuplicatePage Cell (Document Properties Section)](doclockduplicatepage-cell-document-properties-section.md) <br/> |
|DocLockReplace  <br/> |Определяет, следует ли отключить пользовательский интерфейс фигуры замены для этого документа.  <br/> |[DocLockReplace Cell (Document Properties Section)](doclockreplace-cell-document-properties-section.md) <br/> |
|DontMoveChildren  <br/> |Определяет, можно ли перетаскивать фигуры в группе с помощью мыши.  <br/> |[DontMoveChildren Cell (Group Properties Section)](dontmovechildren-cell-group-properties-section.md) <br/> |
|DrawingResizeType  <br/> |Определяет, будет ли страница рисования автоматически меняться в зависимости от схемы.  <br/> |[DrawingResizeType Cell (Page Properties Section)](drawingresizetype-cell-page-properties-section.md) <br/> |
|DrawingScale  <br/> |Представляет значение единицы рисования в текущей шкале рисования.  <br/> |[DrawingScale Cell (Page Properties Section)](drawingscale-cell-page-properties-section.md) <br/> |
|DrawingScaleType  <br/> |Определяет масштаб рисования, выбранный в диалоговом окне "Настройка страницы" (щелкните стрелку "Настройка страницы" на вкладке "Главная").  <br/> |[DrawingScaleType Cell (Page Properties Section)](drawingscaletype-cell-page-properties-section.md) <br/> |
|DrawingSizeType  <br/> |Определяет размер рисунка.  <br/> |[DrawingSizeType Cell (Page Properties Section)](drawingsizetype-cell-page-properties-section.md) <br/> |
|DropOnPageScale  <br/> |Содержит процент масштабирования фигуры при отброшении на страницу рисования.  <br/> |[DropOnPageScale Cell (Miscellaneous Section)](droponpagescale-cell-miscellaneous-section.md) <br/> |
|DynamicsOff  <br/> |Определяет, перемещаются ли перемещаемые фигуры, а соединители перенадвигаются вокруг других фигур и соединители на странице рисования.  <br/> |[DynamicsOff Cell (Page Layout Section)](dynamicsoff-cell-page-layout-section.md) <br/> |
|DynFeedback  <br/> |Изменяет тип визуальной обратной связи, предоставляемой пользователям при перетаскивания соединители.  <br/> |[DynFeedback Cell (Miscellaneous Section)](dynfeedback-cell-miscellaneous-section.md) <br/> |
|EffectSchemeIndex  <br/> |Определяет схему эффекта темы, применяемой к фигуре, в виде integer.  <br/> |[EffectSchemeIndex Cell (Theme Properties Section)](effectschemeindex-cell-theme-properties-section.md) <br/> |
|Висяк  <br/> |Изменяет внешний вид (хронологию) вызовите, контейнеры, временные шкалы и фигуры организационной диаграммы.  <br/> |[EmbellishmentIndex Cell (Theme Properties Section)](embellishmentindex-cell-theme-properties-section.md) <br/> |
|EnableFillProps  <br/> |Определяет, включает ли стиль свойства заливки.  <br/> |[EnableFillProps Cell (Style Properties Section)](enablefillprops-cell-style-properties-section.md) <br/> |
|EnableGrid  <br/> |Определяет, формирует ли приложение фигуры на основе внутренней невидимой сетки страницы при настройке макета в диалоговом окне "Настройка макета".  <br/> |[EnableGrid Cell (Page Layout Section)](enablegrid-cell-page-layout-section.md) <br/> |
|EnableLineProps  <br/> |Определяет, включает ли стиль свойства строки.  <br/> |[EnableLineProps Cell (Style Properties Section)](enablelineprops-cell-style-properties-section.md) <br/> |
|EnableTextProps  <br/> |Определяет, включает ли стиль свойства текста.  <br/> |[EnableTextProps Cell (Style Properties Section)](enabletextprops-cell-style-properties-section.md) <br/> |
|EndArrow  <br/> |Указывает, имеет ли строка стрелку или другой формат конца линии в последней вершине.  <br/> |[EndArrow Cell (Line Format Section)](endarrow-cell-line-format-section.md) <br/> |
|EndArrowSize  <br/> |Определяет размер наконечник в конце строки.  <br/> |[EndArrowSize Cell (Line Format Section)](endarrowsize-cell-line-format-section.md) <br/> |
|EndTrigger  <br/> |Содержит формулу триггера, сгенерированную приложением, которая определяет, следует ли перемещать конечную точку однообразной фигуры для поддержания подключения к другой фигуре.  <br/> |[EndTrigger Cell (Glue Info Section)](endtrigger-cell-glue-info-section.md) <br/> |
|EndX  <br/> |Представляет x-координату конечной точки 1-D фигуры относительно начала родительской фигуры.  <br/> |[EndX Cell (1-D Endpoints Section)](endx-cell-1-d-endpoints-section.md) <br/> |
|EndY  <br/> |Представляет Y-координату конечной точки 1-D фигуры относительно начала родительской фигуры.  <br/> |[EndY Cell (1-D Endpoints Section)](endy-cell-1-d-endpoints-section.md) <br/> |
|EventDblClick  <br/> |Ячейка события, которая оценивается при двойном щелчке по фигуре.  <br/> |[EventDblClick Cell (Events Section)](eventdblclick-cell-events-section.md) <br/> |
|EventDrop  <br/> |Ячейка события, которая оценивается при отброшении фигуры на страницу рисования либо в виде экземпляра, либо при дублировании или вклеии фигуры.  <br/> |[EventDrop Cell (Events Section)](eventdrop-cell-events-section.md) <br/> |
|EventMultiDrop  <br/> |Ячейка события, которая оценивается при отброшении нескольких фигур на страницу рисования в качестве экземпляров или при дублировании или вплеи фигур.  <br/> |[EventMultiDrop Cell (Events Section)](eventmultidrop-cell-events-section.md) <br/> |
|EventXFMod  <br/> |Ячейка события, которая оценивается при преобразовании положения или ориентации фигуры на странице ("XF").  <br/> |[EventXFMod Cell (Events Section)](eventxfmod-cell-events-section.md) <br/> |
|FillBkgnd  <br/> |Определяет цвет, используемый для фона (заливки) шаблона заливки фигуры.  <br/> |[FillBkgnd Cell (Fill Format Section)](fillbkgnd-cell-fill-format-section.md) <br/> |
|FillBkgndTrans  <br/> |Определяет уровень прозрачности для цвета фона (заливки) шаблона заливки фигуры.  <br/> |[FillBkgndTrans Cell (Fill Format Section)](fillbkgndtrans-cell-fill-format-section.md) <br/> |
|FillForegnd  <br/> |Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки фигуры.  <br/> |[FillForegnd Cell (Fill Format Section)](fillforegnd-cell-fill-format-section.md) <br/> |
|FillForegndTrans  <br/> |Определяет уровень прозрачности для цвета фона (заливки) шаблона заливки фигуры.  <br/> |[FillForegndTrans Cell (Fill Format Section)](fillforegndtrans-cell-fill-format-section.md) <br/> |
|FillGradientAngle  <br/> |Определяет угол градиента заливки для градиентов с линейным направлением в градусах.  <br/> |[FillGradientAngle Cell (Gradient Properties Section)](fillgradientangle-cell-gradient-properties-section.md) <br/> |
|FillGradientDir  <br/> |Определяет направление градиента заливки. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.  <br/> |[FillGradientDir Cell (Gradient Properties Section)](fillgradientdir-cell-gradient-properties-section.md) <br/> |
|FillGradientEnabled  <br/> |Определяет, включен ли градиент заливки для этой фигуры.  <br/> |[FillGradientEnabled Cell (Gradient Properties Section)](fillgradientenabled-cell-gradient-properties-section.md) <br/> |
|FillPattern  <br/> |Определяет шаблон заливки для фигуры. Чтобы указать пользовательский шаблон заливки, используйте функцию USE в этой ячейке.  <br/> |[FillPattern Cell (Fill Format Section)](fillpattern-cell-fill-format-section.md) <br/> |
|FlipX  <br/> |Указывает, была ли фигура перевернута по горизонтали.  <br/> |[FlipX Cell (Shape Transform Section)](flipx-cell-shape-transform-section.md) <br/> |
|FlipY  <br/> |Указывает, была ли фигура перевернута вертикально.  <br/> |[FlipY Cell (Shape Transform Section)](flipy-cell-shape-transform-section.md) <br/> |
|FontSchemeIndex  <br/> |Определяет схему шрифтов темы, применяемой к фигуре, в виде integer.  <br/> |[FontSchemeIndex Cell (Theme Properties Section)](fontschemeindex-cell-theme-properties-section.md) <br/> |
|ГАММА  <br/> |Регулировка или исправление интенсивности изображения для конкретного устройства вывода, например монитора или сканера. Значение по умолчанию — 1 (без исправления).  <br/> |[Gamma Cell (Image Properties Section)](gamma-cell-image-properties-section.md) <br/> |
|GlowColor  <br/> |Определяет цвет, используемый для росчерка внешнего свечения, примененного к фигуре, в виде значения RGB или темы.  <br/> |[GlowColor Cell (Additional Effect Properties Section)](glowcolor-cell-additional-effect-properties-section.md) <br/> |
|GlowColorTrans  <br/> |Определяет уровень прозрачности цвета, используемого для росчерка свечения фигуры в процентах.  <br/> |[GlowColorTrans Cell (Additional Effect Properties Section)](glowcolortrans-cell-additional-effect-properties-section.md) <br/> |
|GlowSize  <br/> |Определяет размер внешнего свечения фигуры в точках.  <br/> |[GlowSize Cell (Additional Effect Properties Section)](glowsize-cell-additional-effect-properties-section.md) <br/> |
|GlueType  <br/> |Определяет, использует ли однообразная фигура статический (точка-точка) или динамический (от фигуры к фигуре) при наклеии к другой фигуре.  <br/> |[GlueType Cell (Glue Info Section)](gluetype-cell-glue-info-section.md) <br/> |
|Height  <br/> |Определяет высоту фигуры в единицах рисования.  <br/> |[Height Cell (Shape Transform Section)](height-cell-shape-transform-section.md) <br/> |
|HelpTopic  <br/> |Указывает ид раздела справки фигуры.  <br/> ||
|HideForApply  <br/> |Определяет, где стиль отображается в пользовательском интерфейсе Microsoft Visio.  <br/> |[HideForApply Cell (Style Properties Section)](hideforapply-cell-style-properties-section.md) <br/> |
|HideText  <br/> |Скрывает текст фигуры.  <br/> |[HideText Cell (Miscellaneous Section)](hidetext-cell-miscellaneous-section.md) <br/> |
|ImgHeight  <br/> |Определяет высоту изображения объекта в пределах его границы.  <br/> |[ImgHeight Cell (Foreign Image Info Section)](imgheight-cell-foreign-image-info-section.md) <br/> |
|ImgOffsetX  <br/> |Определяет расстояние, на которое объект смещен по горизонтали от начала границы объекта.  <br/> |[ImgOffsetX Cell (Foreign Image Info Section)](imgoffsetx-cell-foreign-image-info-section.md) <br/> |
|ImgOffsetY  <br/> |Определяет расстояние, на которое объект смещен вертикально от начала границы объекта.  <br/> |[ImgOffsetY Cell (Foreign Image Info Section)](imgoffsety-cell-foreign-image-info-section.md) <br/> |
|ImgWidth  <br/> |Определяет ширину изображения объекта в пределах его границы.  <br/> |[ImgWidth Cell (Foreign Image Info Section)](imgwidth-cell-foreign-image-info-section.md) <br/> |
|InhibitSnap  <br/> |Определяет, будут ли фигуры на странице переднего плана прикреплены к другим объектам на странице и фигурам на фоновой странице.  <br/> |[InhibitSnap Cell (Page Properties Section)](inhibitsnap-cell-page-properties-section.md) <br/> |
|IsDropSource  <br/> |Определяет, можно ли добавить фигуру в группу, перенанося ее в группу.  <br/> |[IsDropSource Cell (Miscellaneous Section)](isdropsource-cell-miscellaneous-section.md) <br/> |
|IsDropTarget  <br/> |Определяет, разрешает ли группа добавлять фигуру в нее, перенанося ее в группу.  <br/> |[IsDropTarget Cell (Group Properties Section)](isdroptarget-cell-group-properties-section.md) <br/> |
|IsSnapTarget  <br/> |Определяет, нужно ли прикрепить группу или фигуры в группе.  <br/> |[IsSnapTarget Cell (Group Properties Section)](issnaptarget-cell-group-properties-section.md) <br/> |
|IsTextEditTarget  <br/> |Определяет назначение текста для группы.  <br/> |[IsTextEditTarget Cell (Group Properties Section)](istextedittarget-cell-group-properties-section.md) <br/> |
|KeepTextFlat  <br/> |Указывает, будет ли текст фигуры игнорировать поворот фигуры в 3-D. Не применяется к 2-D повороту.  <br/> |[KeepTextFlat Cell (3-D Rotation Properties Section)](keeptextflat-cell-3-d-rotation-properties-section.md) <br/> |
|LangID  <br/> |Указывает язык, на котором был введен комментарий.  <br/> |[LangID Cell (Annotation Section)](langid-cell-annotation-section.md) <br/> |
|LangID  <br/> |Указывает язык, на котором был введен текст.  <br/> |[LangID Cell (Character Section)](langid-cell-character-section.md) <br/> |
|LangID  <br/> |Указывает язык, на котором были созданы формулы ячеей.  <br/> |[LangID Cell (Miscellaneous Section)](langid-cell-miscellaneous-section.md) <br/> |
|LangID  <br/> |Указывает язык, на котором ввели значение данных фигуры.  <br/> |[LangID Cell (Shape Data Section)](langid-cell-shape-data-section.md) <br/> |
|LayerMember  <br/> |Указывает членство в уровне фигуры на основе индекса слоев на основе нуля для страницы. Если фигура назначена более чем одному слой, каждый индекс слоя отделяется друг от друга с зачетом.  <br/> ||
|LeftMargin  <br/> |Определяет расстояние между левой границей текстового блока и текстом, который он содержит.  <br/> |[LeftMargin Cell (Text Block Format Section)](leftmargin-cell-text-block-format-section.md) <br/> |
|LineAdjustFrom  <br/> |Определяет, какие динамические соединители, если приложение размескивается, если они маршрутом друг над другом.  <br/> |[LineAdjustFrom Cell (Page Layout Section)](lineadjustfrom-cell-page-layout-section.md) <br/> |
|LineAdjustTo  <br/> |Определяет, какие динамические соединители выровнены друг над другом.  <br/> |[LineAdjustTo Cell (Page Layout Section)](lineadjustto-cell-page-layout-section.md) <br/> |
|LineCap  <br/> |Указывает, скруглили ли строки, квадрат или расширенные строки.  <br/> |[LineCap Cell (Line Format Section)](linecap-cell-line-format-section.md) <br/> |
|LineColor  <br/> |Определяет цвет линии фигуры.  <br/> |[LineColor Cell (Line Format Section)](linecolor-cell-line-format-section.md) <br/> |
|LineColorTrans  <br/> |Определяет уровень прозрачности цвета линии фигуры.  <br/> |[LineColorTrans Cell (Line Format Section)](linecolortrans-cell-line-format-section.md) <br/> |
|LineGradientAngle  <br/> |Определяет угол градиента линии для линейного градиента от 0 до 359,9 градусов.  <br/> |[LineGradientAngle Cell (Gradient Properties Section)](linegradientangle-cell-gradient-properties-section.md) <br/> |
|LineGradientDir  <br/> |Определяет направление градиента линии. Градиент может быть линейным, радиальным, прямоугольным или следовать по пути.  <br/> |[LineGradientDir Cell (Gradient Properties Section)](linegradientdir-cell-gradient-properties-section.md) <br/> |
|LineGradientEnabled  <br/> |Определяет, включен ли градиент линии для линии или границы фигуры.  <br/> |[LineGradientEnabled Cell (Gradient Properties Section)](linegradientenabled-cell-gradient-properties-section.md) <br/> |
|LineJumpCode  <br/> |Определяет соединители, к которым нужно добавить переходы.  <br/> ||
|LineJumpFactorX  <br/> |Определяет размер переходов по горизонтали динамических соединителю на странице относительно значения ячейки LineToLineX. Значение этой ячейки может варьироваться от 0 до 10, но предлагается дробное значение от 0 до 1.  <br/> |[LineJumpFactorX Cell (Page Layout Section)](linejumpfactorx-cell-page-layout-section.md) <br/> |
|LineJumpFactorY  <br/> |Определяет размер переходов по вертикальным динамическим соединителям на странице относительно значения ячейки LineToLineY. Значение этой ячейки может варьироваться от 0 до 10, но предлагается дробное значение от 0 до 1.  <br/> |[LineJumpFactorY Cell (Page Layout Section)](linejumpfactory-cell-page-layout-section.md) <br/> |
|LineJumpStyle  <br/> |Определяет стиль перехода по строке для всех соединитеителей на странице рисования, которые не имеют локального стиля перехода по строкам.  <br/> |[LineJumpStyle Cell (Page Layout Section)](linejumpstyle-cell-page-layout-section.md) <br/> |
|LinePattern  <br/> |Определяет шаблон линии фигуры. Значение, введенного в ячейке LinePattern, — это число, которое является индексом в коллекции шаблонов строк.  <br/> |[LinePattern Cell (Line Format Section)](linepattern-cell-line-format-section.md) <br/> |
|LineRouteExt  <br/> |Определяет внешний вид по умолчанию для всех соединитеителей на странице рисования.  <br/> |[LineRouteExt Cell (Page Layout Section)](linerouteext-cell-page-layout-section.md) <br/> |
|LineToLineX  <br/> |Определяет горизонтальную прорисовку между всеми соединитетелями на странице рисования.  <br/> |[LineToLineX Cell (Page Layout Section)](linetolinex-cell-page-layout-section.md) <br/> |
|LineToLineY  <br/> |Определяет вертикальное разрешение между всеми соединителями на странице рисования.  <br/> |[LineToLineY Cell (Page Layout Section)](linetoliney-cell-page-layout-section.md) <br/> |
|LineToNodeX  <br/> |Определяет горизонтальную прорисовку между всеми соединитетелями и фигурами на странице рисования.  <br/> |[LineToNodeX Cell (Page Layout Section)](linetonodex-cell-page-layout-section.md) <br/> |
|LineToNodeY  <br/> |Определяет вертикальное разрешение между всеми соединителями и фигурами на странице рисования.  <br/> |[LineToNodeY Cell (Page Layout Section)](linetonodey-cell-page-layout-section.md) <br/> |
|LineWeight  <br/> |Определяет вес линии фигуры. Установите вес линии, введите номер с допустимой единицей измерения.  <br/> |[LineWeight Cell (Line Format Section)](lineweight-cell-line-format-section.md) <br/> |
|LocalizeMerge  <br/> |Определяет, локализуются ли фигуры при копировании между документами.  <br/> |[LocalizeMerge Cell (Miscellaneous Section)](localizemerge-cell-miscellaneous-section.md) <br/> |
|LockAspect  <br/> |Блокирует пропорции фигуры, чтобы ее размер был пропорционально; Его нельзя масштабовать в одном измерении.  <br/> |[LockAspect Cell (Protection Section)](lockaspect-cell-protection-section.md) <br/> |
|LockBegin  <br/> |Блокирует точки начала (BeginX, BeginY) размерной фигуры в определенном расположении.  <br/> |[LockBegin Cell (Protection Section)](lockbegin-cell-protection-section.md) <br/> |
|LockCalcWH  <br/> |Блокирует прямоугольник выделения фигуры, чтобы его нельзя было пересчитать при редактировании вершины или при смене типа строки в разделе "Геометрия".  <br/> |[LockCalcWH Cell (Protection Section)](lockcalcwh-cell-protection-section.md) <br/> |
|LockCrop  <br/> |Блокирует объект из другой программы от обрезки средством обрезки.  <br/> |[LockCrop Cell (Protection Section)](lockcrop-cell-protection-section.md) <br/> |
|LockCustProp  <br/> |Определяет, может ли пользователь добавлять, удалять или изменять данные фигур в пользовательском интерфейсе с помощью диалоговых окон "Определение данных фигуры" или ярлыка для окна "Данные фигуры".  <br/> |[LockCustProp Cell (Protection Section)](lockcustprop-cell-protection-section.md) <br/> |
|LockDelete  <br/> |Блокирует фигуру, чтобы ее нельзя было удалить.  <br/> |[LockDelete Cell (Protection Section)](lockdelete-cell-protection-section.md) <br/> |
|LockEnd  <br/> |Блокирует конечную точку (EndX, EndY) размерной фигуры в определенном расположении.  <br/> |[LockEnd Cell (Protection Section)](lockend-cell-protection-section.md) <br/> |
|LockFormat  <br/> |Блокирует форматирование фигуры, поэтому ее нельзя изменить.  <br/> |[LockFormat Cell (Protection Section)](lockformat-cell-protection-section.md) <br/> |
|LockFromGroupFormat  <br/> |Блокирует распространение изменений формата в фигуры группы на подформы, при этом позволяя пользователям форматировать выбранные под фигуры напрямую. Значение ячейки LockFromGroupFormat соответствует параметру "От" в диалоговом окне "Защита".  <br/> |[LockFromGroupFormat Cell (Protection Section)](lockfromgroupformat-cell-protection-section.md) <br/> |
|LockGroup  <br/> |Блокирует группу, чтобы ее нельзя было отгруппировать.  <br/> |[LockGroup Cell (Protection Section)](lockgroup-cell-protection-section.md) <br/> |
|LockHeight  <br/> |Блокирует высоту фигуры, чтобы ее высота оставалась неизменной при изменениях размера фигуры.  <br/> |[LockHeight Cell (Protection Section)](lockheight-cell-protection-section.md) <br/> |
|LockMoveX  <br/> |Блокирует горизонтальное положение фигуры, поэтому ее невозможно по горизонтали.  <br/> |[LockMoveX Cell (Protection Section)](lockmovex-cell-protection-section.md) <br/> |
|LockMoveY  <br/> |Блокирует вертикальное положение фигуры, поэтому ее невозможно перемещать по вертикали.  <br/> |[LockMoveY Cell (Protection Section)](lockmovey-cell-protection-section.md) <br/> |
|LockPreview  <br/> |Определяет, сохраняется ли предварительный просмотр при каждом сохранения рисунка.  <br/> |[LockPreview Cell (Document Properties Section)](lockpreview-cell-document-properties-section.md) <br/> |
|LockReplace  <br/> |Указывает, может ли фигура участвовать в операции замены (в качестве целевой или заменяемой фигуры).  <br/> |[LockReplace Cell (Protection Section)](lockreplace-cell-protection-section.md) <br/> |
|LockRotate  <br/> |Блокирует поворачивать двухградивные фигуры с помощью вращающегося левого 90° или поворота вправо на 90°.  <br/> |[LockRotate Cell (Protection Section)](lockrotate-cell-protection-section.md) <br/> |
|LockSelect  <br/> |Предотвращает выбор фигуры.  <br/> |[LockSelect Cell (Protection Section)](lockselect-cell-protection-section.md) <br/> |
|LockTextEdit  <br/> |Блокирует текст фигуры, чтобы его нельзя было редактировать.  <br/> |[LockTextEdit Cell (Protection Section)](locktextedit-cell-protection-section.md) <br/> |
|LockThemeColors  <br/> |Предотвращает применение цветов темы к фигуре. Значение ячейки LockThemeColors соответствует параметру "Цвета темы от" в диалоговом окне "Защита".  <br/> |[LockThemeColors Cell (Protection Section)](lockthemecolors-cell-protection-section.md) <br/> |
|LockThemeConnectors  <br/> |Предотвращает изменение ячейки ConnectorsSchemeIndex в строке "Свойства темы" путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.  <br/> |[LockThemeConnectors Cell (Protection Section)](lockthemeconnectors-cell-protection-section.md) <br/> |
|LockThemeEffects  <br/> |Соответствует параметру "Эффекты темы" в диалоговом окне "Защита".  <br/> |[LockThemeEffects Cell (Protection Section)](lockthemeeffects-cell-protection-section.md) <br/> |
|LockThemeFonts  <br/> |Предотвращает изменение ячейки FontIndex в строке "Свойства темы" путем применения новой темы. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.  <br/> |[LockThemeFonts Cell (Protection Section)](lockthemefonts-cell-protection-section.md) <br/> |
|LockThemeIndex  <br/> |Предотвращает изменение ячейки ThemeIndex в строке "Свойства темы" путем применения новой темы или выбора новой схемы соединителя. Не мешает пользователям вручную редактировать это значение в таблице shapeSheet.  <br/> |[LockThemeIndex Cell (Protection Section)](lockthemeindex-cell-protection-section.md) <br/> |
|LockVariation  <br/> |Определяет, можно ли изменить вариант темы, примененный к странице или фигуре, в качестве boolean.  <br/> |[LockVariation Cell (Protection Section)](lockvariation-cell-protection-section.md) <br/> |
|LockVtxEdit  <br/> |Блокирует вершины фигуры, чтобы их нельзя было редактировать.  <br/> |[LockVtxEdit Cell (Protection Section)](lockvtxedit-cell-protection-section.md) <br/> |
|LockWidth  <br/> |Блокирует ширину фигуры, чтобы ее ширина оставалась неизменной при ее размере.  <br/> |[LockWidth Cell (Protection Section)](lockwidth-cell-protection-section.md) <br/> |
|LocPinX  <br/> |Представляет x-координату закрепления фигуры (центра поворота) относительно начала фигуры. Формула по умолчанию для определения LocPinX: = \* Ширина 0,5.  <br/> |[LocPinX Cell (Shape Transform Section)](locpinx-cell-shape-transform-section.md) <br/> |
|LockPinY  <br/> |Представляет Y-координату закрепления фигуры (центра поворота) относительно начала фигуры. Формула по умолчанию для определения LocPinY: = Высота \* 0,5.  <br/> |[LocPinY Cell (Shape Transform Section)](locpiny-cell-shape-transform-section.md) <br/> |
|NoAlignBox  <br/> |Включает и выключает отображение прямоугольника выбора для выбранной фигуры.  <br/> |[NoAlignBox Cell (Miscellaneous Section)](noalignbox-cell-miscellaneous-section.md) <br/> |
|NoCoauth  <br/> |Определяет, может ли документ, хранимый на сервере SharePoint 2013 или в Microsoft OneDrive, одновременно редактироваться несколькими авторами в сеансе совместной работы.  <br/> |[NoCoauth Cell (Document Properties Section)](nocoauth-cell-document-properties-section.md) <br/> |
|NoCtlHandles  <br/> |Предотвращает появления химок управления при выборе фигуры.  <br/> |[NoCtlHandles Cell (Miscellaneous Section)](noctlhandles-cell-miscellaneous-section.md) <br/> |
|NoLiveDynamics  <br/> |Определяет, динамически ли размер фигуры меняется или поворачивается при ее обработке.  <br/> |[NoLiveDynamics Cell (Miscellaneous Section)](nolivedynamics-cell-miscellaneous-section.md) <br/> |
|NonPrinting  <br/> |Включает и выключает печать для выбранной фигуры.  <br/> |[NonPrinting Cell (Miscellaneous Section)](nonprinting-cell-miscellaneous-section.md) <br/> |
|NoObjHandles  <br/> |Переключает отображение десков выбора для выбранной фигуры.  <br/> |[NoObjHandles Cell (Miscellaneous Section)](noobjhandles-cell-miscellaneous-section.md) <br/> |
|NoProofing  <br/> |Определите, будет ли орфографическая ошибка автоматически исправлена и будут ли отображаться ошибки орфографии для выбранной фигуры.  <br/> ||
|ObjType  <br/> |Определяет, можно ли разместить объекты или маршрутизать их на схемах при использовании диалоговых окна "Настройка макета" для разметки фигур.  <br/> |[ObjType Cell (Miscellaneous Section)](objtype-cell-miscellaneous-section.md) <br/> |
|OnPage  <br/> |Указывает, печатается ли рисунок на определенном количестве страниц принтера.  <br/> |[OnPage Cell (Print Properties Section)](onpage-cell-print-properties-section.md) <br/> |
|OutputFormat  <br/> |Определяет формат выходных данных для рисования. Страницы рисования обычно форматированы для печати (по умолчанию); однако можно выбрать другие форматы выходных данных.  <br/> |[OutputFormat Cell (Document Properties Section)](outputformat-cell-document-properties-section.md) <br/> |
|PageBottomMargin  <br/> |Указывает поле в нижней части печатной страницы.  <br/> |[PageBottomMargin Cell (Print Properties Section)](pagebottommargin-cell-print-properties-section.md) <br/> |
|PageHeight  <br/> |Содержит высоту печатной страницы в единицах рисования.  <br/> |[PageHeight Cell (Page Properties Section)](pageheight-cell-page-properties-section.md) <br/> |
|PageLeftMargin  <br/> |Указывает поле слева от печатаемой страницы.  <br/> |[PageLeftMargin Cell (Print Properties Section)](pageleftmargin-cell-print-properties-section.md) <br/> |
|PageLineJumpDirX  <br/> |Определяет направление переходов по горизонтальным динамическим соединитетелям на странице рисования, к которой не применено локальное направление перехода.  <br/> |[PageLineJumpDirX Cell (Page Layout Section)](pagelinejumpdirx-cell-page-layout-section.md) <br/> |
|PageLineJumpDiry  <br/> |Определяет направление переходов по вертикальным динамическим соединителям на странице рисования, к которой не применено локальное направление перехода.  <br/> |[PageLineJumpDirY Cell (Page Layout Section)](pagelinejumpdiry-cell-page-layout-section.md) <br/> |
|PageLockDuplicate  <br/> |Определяет, можно ли дублировать страницу в качестве boolean.  <br/> |[PageLockDuplicate Cell (Page Properties Section)](pagelockduplicate-cell-page-properties-section.md) <br/> |
|PageLockReplace  <br/> |Указывает, следует ли отключить кнопку "Заменить фигуру" для этой страницы.  <br/> |[PageLockReplace Cell (Page Properties Section)](pagelockreplace-cell-page-properties-section.md) <br/> |
|PageRightMargin  <br/> |Указывает поле справа от печатной страницы.  <br/> |[PageRightMargin Cell (Print Properties Section)](pagerightmargin-cell-print-properties-section.md) <br/> |
|PageScale  <br/> |Определяет значение единицы страницы в текущей шкале рисования. Масштаб рисования для страницы — это соотношение единицы, показанной в ячейке PageScale, к единице рисования, показанной в ячейке DrawingScale.  <br/> |[PageScale Cell (Page Properties Section)](pagescale-cell-page-properties-section.md) <br/> |
|PageShapeSplit  <br/> |Указывает, можно ли автоматически разделить фигуры на странице.  <br/> |[PageShapeSplit Cell (Page Layout Section)](pageshapesplit-cell-page-layout-section.md) <br/> |
|PagesX  <br/> |Определяет количество страниц принтера, на которых страница рисунка помещается горизонтально.  <br/> |[PagesX Cell (Print Properties Section)](pagesx-cell-print-properties-section.md) <br/> |
|PagesY  <br/> |Определяет количество страниц принтера, на которых страница рисунка помещается вертикально.  <br/> |[PagesY Cell (Print Properties Section)](pagesy-cell-print-properties-section.md) <br/> |
|PageTopMargin  <br/> |Указывает поле в верхней части страницы принтера.  <br/> |[PageTopMargin Cell (Print Properties Section)](pagetopmargin-cell-print-properties-section.md) <br/> |
|PageWidth  <br/> |Определяет ширину печатных страниц в единицах рисования.  <br/> |[PageWidth Cell (Page Properties Section)](pagewidth-cell-page-properties-section.md) <br/> |
|PaperKind  <br/> |Указывает тип бумаги, на которой будет печататься страница.  <br/> |[PaperKind Cell (Print Properties Section)](paperkind-cell-print-properties-section.md) <br/> |
|PaperSource  <br/> |Определяет источник бумаги для страницы.  <br/> |[PaperSource Cell (PrintProperties Section)](papersource-cell-printproperties-section.md) <br/> |
|Perspective  <br/> |Определяет угол перспективы для поворота перспективы в градусах (от 0 до 359,9).  <br/> |[Perspective Cell (3-D Rotation Properties Section)](perspective-cell-3-d-rotation-properties-section.md) <br/> |
|PinX  <br/> |Представляет x-координату закрепления фигуры (центра поворота) относительно начала родительского.  <br/> |[PinX Cell (Shape Transform Section)](pinx-cell-shape-transform-section.md) <br/> |
|PinY  <br/> |Представляет координату Y закрепления фигуры (центра поворота) относительно начала родительского.  <br/> |[PinY Cell (Shape Transform Section)](piny-cell-shape-transform-section.md) <br/> |
|PlaceDepth  <br/> |Определяет метод, с помощью которого анализировался рисунок перед созданием макета, и определяет тип макета.  <br/> |[PlaceDepth Cell (Page Layout Section)](placedepth-cell-page-layout-section.md) <br/> |
|PlaceFlip  <br/> |Определяет, как можно пролистыть и/или повернуть фигуры на странице при использовании диалогового окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout страницу, а затем щелкните "Дополнительные параметры макета").  <br/> |[PlaceFlip Cell (Page Layout Section)](placeflip-cell-page-layout-section.md) <br/> |
|PlaceStyle  <br/> |Определяет, как фигуры помещаются на страницу при размещении фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout", а затем щелкните "Дополнительные параметры макета").  <br/> |[PlaceStyle Cell (Page Layout Section)](placestyle-cell-page-layout-section.md) <br/> |
|PlowCode  <br/> |Определяет, перемещаются ли вмежаемые фигуры, когда вы передвигаете их рядом с другой замесяемой фигурой на странице рисования.  <br/> |[PlowCode Cell (Page Layout Section)](plowcode-cell-page-layout-section.md) <br/> |
|PreviewQuality  <br/> |Определяет, является ли предварительный просмотр черновика качеством или подробным.  <br/> |[PreviewQuality Cell (Document Properties Section)](previewquality-cell-document-properties-section.md) <br/> |
|PreviewScope  <br/> |Определяет, включает ли ваш рисунок предварительный просмотр. Если в вашем рисунке есть предварительный просмотр, он определяет, будет ли в режиме предварительного просмотра показана только первая страница или все страницы в этом рисунке.  <br/> |[PreviewScope Cell (Document Properties Section)](previewscope-cell-document-properties-section.md) <br/> |
|PrintGrid  <br/> |Указывает, следует ли печатать сетку при печати страницы документа.  <br/> |[PrintGrid Cell (Print Properties Section)](printgrid-cell-print-properties-section.md) <br/> |
|PrintPageOrientation  <br/> |Определяет, печатается ли страница с помощью кантной или альбомной ориентации.  <br/> |[PrintPageOrientation Cell (Print Properties Section)](printpageorientation-cell-print-properties-section.md) <br/> |
|QuickStyleEffectsMatrix  <br/> |Определяет эффекты быстрого стиля, которые фигура наследует от активной темы, в виде integer от 0 до 6.  <br/> ||
|QuickStyleFillColor  <br/> |Определяет цвет темы, который использует заливка фигуры, в виде integer от 0 до 7.  <br/> |[QuickStyleFillColor Cell (Quick Style Section)](quickstylefillcolor-cell-quick-style-section.md) <br/> |
|QuickStyleFillMatrix  <br/> |Определяет стиль заливки "Быстрый стиль", наследуемый фигурой от активной темы, в виде integer от 0 до 6.  <br/> |[QuickStyleFillMatrix Cell (Quick Style Section)](quickstylefillmatrix-cell-quick-style-section.md) <br/> |
|QuickStyleFontColor  <br/> |Определяет цвет шрифта из быстрых стилей, наследуемый текстом фигуры от активной темы, в виде integer от 0 до 1.  <br/> |[QuickStyleFontColor Cell (Quick Style Section)](quickstylefontcolor-cell-quick-style-section.md) <br/> |
|QuickStyleFontMatrix  <br/> |Определяет стиль шрифта для каждого быстрого стиля в качестве integer от 1 до 6.  <br/> |[QuickStyleFontMatrix Cell (Quick Style Section)](quickstylefontmatrix-cell-quick-style-section.md) <br/> |
|QuickStyleLineColor  <br/> |Определяет цвет темы, который использует линия фигуры, в виде integer от 0 до 7.  <br/> |[QuickStyleLineColor Cell (Quick Style Section)](quickstylelinecolor-cell-quick-style-section.md) <br/> |
|QuickStyleLineMatrix  <br/> |Определяет стиль строки "Быстрый стиль", наследуемый фигурой, в виде integer от 0 до 6.  <br/> |[QuickStyleLineMatrix Cell (Quick Style Section)](quickstylelinematrix-cell-quick-style-section.md) <br/> |
|QuickStyleShadowColor  <br/> |Определяет цвет темы, который использует тени фигуры, в виде integer от 0 до 7.  <br/> |[QuickStyleShadowColor Cell (Quick Style Section)](quickstyleshadowcolor-cell-quick-style-section.md) <br/> |
|QuickStyleType  <br/> |Определяет тип quick Style (2-мерный, 1-мерный или соединители), наследуемый фигурой.  <br/> |[QuickStyleType Cell (Quick Style Section)](quickstyletype-cell-quick-style-section.md) <br/> |
|QuickStyleVariation  <br/> |Обеспечивает видимость цвета текста, строки и/или заливки фигуры на фоне темной схемы.  <br/> ||
|ReflectionBlur  <br/> |Определяет количество размытия для отражения фигуры в точках от 0,0 до 100,0.  <br/> |[ReflectionBlur Cell (Additional Effect Properties Section)](reflectionblur-cell-additional-effect-properties-section.md) <br/> |
|ReflectionDist  <br/> |Определяет расстояние, на которое смещено отражение от фигуры в пунктах от 0,0 до 100,0.  <br/> |[ReflectionDist Cell (Additional Effect Properties Section)](reflectiondist-cell-additional-effect-properties-section.md) <br/> |
|ReflectionSize  <br/> |Определяет размер отражения относительно фигуры в процентах от 0,0 до 100,0%. Фигура со значением 0 % в ячейке ReflectionSize не имеет отражения; Значение 100 % отображает полное зеркальное изображение фигуры.  <br/> |[ReflectionSize Cell (Additional Effect Properties Section)](reflectionsize-cell-additional-effect-properties-section.md) <br/> |
|ReflectionTrans  <br/> |Определяет прозрачность отражения в процентах от 0 до 100 %.  <br/> |[ReflectionTrans Cell (Additional Effect Properties Section)](reflectiontrans-cell-additional-effect-properties-section.md) <br/> |
|Связи  <br/> |Хранит связи между контейнерами, списками, вызовами и фигурами.  <br/> |[Relationships Cell (Shape Layout Section)](relationships-cell-shape-layout-section.md) <br/> |
|ReplaceCopyCells  <br/> |Указывает список ячеек в таблице shapeSheet, скопированные из старой фигуры в фигуру замены во время операции замены фигуры.  <br/> |[ReplaceCopyCells Cell (Change Shape Behavior Section)](replacecopycells-cell-change-shape-behavior-section.md) <br/> |
|ReplaceLockFormat  <br/> |Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. Если для ячейки ReplaceLockFormat для фигуры-хозяина установлено значение TRUE (1), значения форматирования хозяина заменяют все соответствующие значения фигуры, заменяемой хозяином.  <br/> |[ReplaceLockFormat Cell (Change Shape Behavior Section)](replacelockformat-cell-change-shape-behavior-section.md) <br/> |
|ReplaceLockShapeData  <br/> |Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. ReplaceLockShapeData определяет, переопределяются ли все данные фигуры заменяемой фигуры.  <br/> |[ReplaceLockShapeData Cell (Change Shape Behavior Section)](replacelockshapedata-cell-change-shape-behavior-section.md) <br/> |
|ReplaceLockText  <br/> |Указывает, переоценили ли значения указанных ячеек в фигуре хозяина значения (включая локальные значения) фигуры, заменяемой во время операции замены фигуры. ReplaceLockText определяет, переопределяется ли текст, отображаемого на мастере, текст заменяемой фигуры.  <br/> |[ReplaceLockText Cell (Change Shape Behavior Section)](replacelocktext-cell-change-shape-behavior-section.md) <br/> |
|ResizeMode  <br/> |Показывает текущее поведение изменения размеров фигуры.  <br/> |[ResizeMode Cell (Shape Transform Section)](resizemode-cell-shape-transform-section.md) <br/> |
|ResizePage  <br/> |Определяет, следует ли увеличивать страницу, чтобы заключить рисунок после складки фигур, с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout page, а затем щелкните "Дополнительные параметры макета").  <br/> |[ResizePage Cell (Page Layout Section)](resizepage-cell-page-layout-section.md) <br/> |
|RightMargin  <br/> |Определяет расстояние между правой границей текстового блока и текстом, который он содержит. Значение по умолчанию — 0,1 дюйма.  <br/> |[RightMargin Cell (Text Block Format Section)](rightmargin-cell-text-block-format-section.md) <br/> |
|RotateGradientWithShape  <br/> |Определяет, вращается ли градиент заливки фигурой в 2D-повороте в виде boolean.  <br/> |[RotateGradientWithShape Cell (Gradient Properties Section)](rotategradientwithshape-cell-gradient-properties-section.md) <br/> |
|RotationType  <br/> |Определяет, следует ли фигура параллельному повороту, повороту перспективы или повороту косой точки в виде одного или того же друг другу в виде 0–6.  <br/> |[RotationType Cell (3-D Rotation Properties Section)](rotationtype-cell-3-d-rotation-properties-section.md) <br/> |
|RotationXAngle  <br/> |Определяет угол поворота вдоль оси X в градусах (от 0,0 до 359,9).  <br/> |[RotationXAngle Cell (3-D Rotation Properties Section)](rotationxangle-cell-3-d-rotation-properties-section.md) <br/> |
|RotationYAngle  <br/> |Определяет угол поворота вдоль оси Y в градусах (от 0,0 до 359,9).  <br/> |[RotationYAngle Cell (3-D Rotation Properties Section)](rotationyangle-cell-3-d-rotation-properties-section.md) <br/> |
|RotationZAngle  <br/> |Определяет угол поворота вдоль оси Z в градусах (от 0,0 до 359,9).  <br/> |[RotationZAngle Cell (3-D Rotation Properties Section)](rotationzangle-cell-3-d-rotation-properties-section.md) <br/> |
|Округление  <br/> |Указывает радиус применяемой дуги округлки, где встречаются два контиговых сегмента пути. Например, округление можно использовать для придания прямоугольнику скругленных углов. Чтобы установить округлку, введите значение с единицами измерения (пара число-единица).  <br/> |[Rounding Cell (Line Format Section)](rounding-cell-line-format-section.md) <br/> |
|RouteStyle  <br/> |Определяет стиль и направление маршрутов для всех соединитеителей на странице рисования, которые не имеют локального стиля маршрутки.  <br/> |[RouteStyle Cell (Page Layout Section)](routestyle-cell-page-layout-section.md) <br/> |
|ScaleX  <br/> |Указывает процент увеличения страницы рисования на странице принтера.  <br/> |[ScaleX Cell (Print Properties Section)](scalex-cell-print-properties-section.md) <br/> |
|ScaleY  <br/> |Указывает процент увеличения страницы рисования на странице принтера.  <br/> |[ScaleY Cell (Print Properties Section)](scaley-cell-print-properties-section.md) <br/> |
|SelectMode  <br/> |Определяет, как выбрать фигуру группы и ее члены.  <br/> |[SelectMode Cell (Group Properties Section)](selectmode-cell-group-properties-section.md) <br/> |
|ShapeFixedCode Cell  <br/> |Определяет поведение размещения для размещения фигуры.  <br/> |[ShapeFixedCode Cell (Shape Layout Section)](shapefixedcode-cell-shape-layout-section.md) <br/> |
|ShapeKeywords  <br/> |Содержит ключевые слова поиска, которые были назначены этаковой фигуре.  <br/> ||
|ShapePermeablePlace  <br/> |Определяет, можно ли размещать размещаемые фигуры поверх фигуры при размещении фигур в диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout page и выберите "Дополнительные параметры макета").  <br/> |[ShapePermeablePlace Cell (Shape Layout Section)](shapepermeableplace-cell-shape-layout-section.md) <br/> |
|ShapePermeableX  <br/> |Определяет, может ли соединителю маршрут следования по горизонтали проходить через заметоряемую фигуру.  <br/> |[ShapePermeableX Cell (Shape Layout Section)](shapepermeablex-cell-shape-layout-section.md) <br/> |
|ShapePermeableY  <br/> |Определяет, может ли соединитель проходить по вертикали через фигуру.  <br/> |[ShapePermeableY Cell (Shape Layout Section)](shapepermeabley-cell-shape-layout-section.md) <br/> |
|ShapePlaceFlip  <br/> |Определяет, как подкладываемая фигура пролистывает, поворачивается или и то, и другое на странице при выкладывке фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета").  <br/> |[ShapePlaceFlip Cell (Shape Layout Section)](shapeplaceflip-cell-shape-layout-section.md) <br/> |
|ShapePlaceStyle  <br/> |Указывает, как фигуры помещаются на страницу при размещении фигур в диалоговом окне "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета"). Хранит значения стиля макета и выравнивания из VisCellIndices.  <br/> |[ShapePlaceStyle Cell (Shape Layout Section)](shapeplacestyle-cell-shape-layout-section.md) <br/> |
|ShapePlowCode  <br/> |Определяет, перемещается ли эта замежаемая фигура, когда вы передвигаете другую фигуру рядом с этой фигурой на странице рисования.  <br/> |[ShapePlowCode Cell (Shape Layout Section)](shapeplowcode-cell-shape-layout-section.md) <br/> |
|ShapeRouteStyle  <br/> |Определяет стиль и направление маршрутки для выбранного соединитела на странице рисования.  <br/> |[ShapeRouteStyle Cell (Shape Layout Section)](shaperoutestyle-cell-shape-layout-section.md) <br/> |
|ShapeShdwBlur  <br/> |Определяет размер размытия для тени фигуры в пунктах (от 0,00 до 100,00).  <br/> |[ShapeShdwBlur Cell (Fill Format Section)](shapeshdwblur-cell-fill-format-section.md) <br/> |
|ShapeShdwObliqueAngle  <br/> |Указывает угол наклонного направления тени фигуры.  <br/> |[ShapeShdwObliqueAngle Cell (Fill Format Section)](shapeshdwobliqueangle-cell-fill-format-section.md) <br/> |
|ShapeShdwOffsetX  <br/> |Определяет расстояние в единицах страницы, на которое тень фигуры смещена по горизонтали от фигуры.  <br/> |[ShapeShdwOffsetX Cell (Fill Format Section)](shapeshdwoffsetx-cell-fill-format-section.md) <br/> |
|ShapeShdwOffsetY  <br/> |Определяет расстояние в единицах страницы, на которое по вертикали смещена тень фигуры.  <br/> |[ShapeShdwOffsetY Cell (Fill Format Section)](shapeshdwoffsety-cell-fill-format-section.md) <br/> |
|ShapeShdwScaleFactor  <br/> |Указывает процент увеличения или уменьшения тени фигуры.  <br/> |[ShapeShdwScaleFactor Cell (Fill Format Section)](shapeshdwscalefactor-cell-fill-format-section.md) <br/> |
|ShapeShdwShow  <br/> |Определяет, отображает ли фигура тень в виде integer от 0 до 2.  <br/> |[ShapeShdwShow Cell (Fill Format Section)](shapeshdwshow-cell-fill-format-section.md) <br/> |
|ShapeShdwType  <br/> |Указывает тип тени для фигуры.  <br/> |[ShapeShdwType Cell (Fill Format Section)](shapeshdwtype-cell-fill-format-section.md) <br/> |
|ShapeSplit  <br/> |Указывает, может ли эта фигура разделять фигуры, которые можно разделить.  <br/> |[ShapeSplit Cell (Shape Layout Section)](shapesplit-cell-shape-layout-section.md) <br/> |
|ShapeSplittable  <br/> |Указывает, можно ли разделить эту 1-D-фигуру.  <br/> |[ShapeSplittable Cell (Shape Layout Section)](shapesplittable-cell-shape-layout-section.md) <br/> |
|Sharpen  <br/> |Толстрирования тол рисунка. Значение по умолчанию — 0%. Резкое увеличение изображения фокусирует его, увеличив контрастность смежных пикселей.  <br/> |[Sharpen Cell (Image Properties Section)](sharpen-cell-image-properties-section.md) <br/> |
|ShdwForegnd  <br/> |Определяет цвет, используемый для переднего плана (росчерка) шаблона заливки тени для перепада фигуры.  <br/> |[ShdwForegnd Cell (Fill Format Section)](shdwforegnd-cell-fill-format-section.md) <br/> |
|ShdwForegndTrans  <br/> |Определяет уровень прозрачности для цвета, используемого для переднего плана (росчерка) шаблона заливки тени для отпадения фигуры.  <br/> |[ShdwForegndTrans Cell (Fill Format Section)](shdwforegndtrans-cell-fill-format-section.md) <br/> |
|ShdwObliqueAngle  <br/> |Содержит число, определяющие угол наклонного направления при применении типа теней страницы по умолчанию.  <br/> |[ShdwObliqueAngle Cell (Page Properties Section)](shdwobliqueangle-cell-page-properties-section.md) <br/> |
|ShdwOffsetX  <br/> |Определяет расстояние в единицах страницы, на которое тень фигуры смещена по горизонтали от фигуры.  <br/> |[ShdwOffsetX Cell (Page Properties Section)](shdwoffsetx-cell-page-properties-section.md) <br/> |
|ShdwOffsetY  <br/> |Определяет расстояние в единицах страницы, на которое тень фигуры вертикально смещена от фигуры.  <br/> |[ShdwOffsetY Cell (Page Properties Section)](shdwoffsety-cell-page-properties-section.md) <br/> |
|ShdwPattern  <br/> |Определяет шаблон заливки для тени фигуры.  <br/> |[ShdwPattern Cell (Fill Format Section)](shdwpattern-cell-fill-format-section.md) <br/> |
|ShdwScaleFactor  <br/> |Указывает процент для увеличения или уменьшения тени фигуры.  <br/> |[ShdwScaleFactor Cell (Page Properties Section)](shdwscalefactor-cell-page-properties-section.md) <br/> |
|ShdwType  <br/> |Указывает тип теней по умолчанию для страницы.  <br/> |[ShdwType Cell (Page Properties Section)](shdwtype-cell-page-properties-section.md) <br/> |
|SketchAmount  <br/> |Определяет искажение эффекта наброска в качестве количества от 0 до 25.  <br/> |[SketchAmount Cell (Additional Effect Properties Section)](sketchamount-cell-additional-effect-properties-section.md) <br/> |
|SketchEnabled  <br/> |Определяет, отображается ли эффект наброска на фигуре в виде boolean.  <br/> |[SketchEnabled Cell (Additional Effect Properties Section)](sketchenabled-cell-additional-effect-properties-section.md) <br/> |
|SketchFillChange  <br/> |Определяет объем случайного выбора заливки фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела. Если значение ячейки SketchFillChange составляет 0 %, вязая геометрия заливки фигуры соответствует геометрии фигуры. Если значение составляет 100 %, ограниченная геометрия заливки фигуры не следует за геометрией фигуры.  <br/> |[SketchFillChange Cell (Additional Effect Properties Section)](sketchfillchange-cell-additional-effect-properties-section.md) <br/> |
|SketchLineChange  <br/> |Определяет объем случайного выбора линии фигуры из геометрии фигуры при использовании эффекта наброска в процентах от длины раздела. Если значение ячейки SketchLineChange — 0%, геометрия линии фигуры соответствует геометрии фигуры. Если значение составляет 100 %, геометрия линии фигуры не следует за геометрией фигуры.  <br/> |[SketchLineChange Cell (Additional Effect Properties Section)](sketchlinechange-cell-additional-effect-properties-section.md) <br/> |
|SketchLineWeight  <br/> |Определяет дополнительную толщину, добавленную в вес линии в результате наброска в пунктах от 0 до 50. Толщина линии фигуры увеличивается по мере увеличения значения ячейки SketchLineWeight.  <br/> |[SketchLineWeight Cell (Additional Effect Properties Section)](sketchlineweight-cell-additional-effect-properties-section.md) <br/> |
|SketchSeed  <br/> |Представляет значение случайности, используемого для определения геометрии эффекта наброска, в качестве положительного значения. Значение ячейки SketchSeed создается случайным образом, когда к фигуре применяется эффект наброска.  <br/> |[SketchSeed Cell (Additional Effect Properties Section)](sketchseed-cell-additional-effect-properties-section.md) <br/> |
|SoftEdgesSize  <br/> |Определяет размер эффекта мягкого края в пунктах от 0,00 до 100,00. Если ячейка SoftEdgesSize имеет значение 0, фигура не имеет мягких ребра.  <br/> |[SoftEdgesSize Cell (Additional Effect Properties Section)](softedgessize-cell-additional-effect-properties-section.md) <br/> |
|TextBkgnd  <br/> |Определяет цвет фона текста для фигуры.  <br/> |[TextBkgnd Cell (Text Block Format Section)](textbkgnd-cell-text-block-format-section.md) <br/> |
|TextBkgndTrans  <br/> |Определяет уровень прозрачности для цвета фона текстового блока фигуры.  <br/> |[TextBkgndTrans Cell (Text Block Format Section)](textbkgndtrans-cell-text-block-format-section.md) <br/> |
|TextDirection  <br/> |Определяет направление символов в текстовом блоке.  <br/> |[TextDirection Cell (Text Block Format Section)](textdirection-cell-text-block-format-section.md) <br/> |
|TheData  <br/> |Зарезервировано для последующего использования.  <br/> |[TheData Cell (Events Section)](thedata-cell-events-section.md) <br/> |
|ThemeIndex  <br/> |Сохраняет в качестве всего 100 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 000 . Если для документа выбрана новая тема, ячейка ThemeIndex для документа, а также все страницы и фигуры, которые он содержит, обновляется с помощью индекса встроенной темы.  <br/> |[ThemeIndex Cell (Theme Properties Section)](themeindex-cell-theme-properties-section.md) <br/> |
|TheText  <br/> |Ячейка события, которая оценивается при смене текста или текстовой композиции фигуры.  <br/> |[TheText Cell (Events Section)](thetext-cell-events-section.md) <br/> |
|TopMargin  <br/> |Определяет расстояние между верхней границей текстового блока и первой строкой текста в нем. Значение по умолчанию — 4,0000. Это значение не зависит от масштаба рисования. При масштабе рисования верхнее поле остается тем же.  <br/> |[TopMargin Cell (Text Block Format Section)](topmargin-cell-text-block-format-section.md) <br/> |
|Прозрачность  <br/> |Определяет уровень прозрачности для диапазона цвета текста фигуры.  <br/> |[Transparency Cell (Character Section)](transparency-cell-character-section.md) <br/> |
|Прозрачность  <br/> |Определяет уровень прозрачности для цвета слоя.  <br/> |[Transparency Cell (Image Properties Section)](transparency-cell-image-properties-section.md) <br/> |
|Прозрачность  <br/> |Определяет уровень прозрачности для цвета слоя.  <br/> |[Transparency Cell (Layers Section)](transparency-cell-layers-section.md) <br/> |
|TxtAngle  <br/> |Определяет текущий угол поворота текстового блока относительно оси X фигуры. Значение по умолчанию — 0 градусов.  <br/> |[TxtAngle Cell (Text Transform Section)](txtangle-cell-text-transform-section.md) <br/> |
|TxtHeight  <br/> |Определяет высоту текстового блока. Формула по умолчанию: = Height \* 1  <br/> |[TxtHeight Cell (Text Transform Section)](txtheight-cell-text-transform-section.md) <br/> |
|TxtLocPinX  <br/> |Определяет x-координату центра вращения текстового блока относительно начала текстового блока. Формула по умолчанию: = TxtWidth 0.5This формула оценивается в горизонтальном \* центре текстового блока.  <br/> |[TxtLocPinX Cell (Text Transform Section)](txtlocpinx-cell-text-transform-section.md) <br/> |
|TxtLocPinY  <br/> |Определяет Y-координату центра вращения текстового блока относительно начала текстового блока. Формула по умолчанию: = TxtHeight \* 0.5  <br/> |[TxtLocPinY Cell (Text Transform Section)](txtlocpiny-cell-text-transform-section.md) <br/> |
|TxtPinX  <br/> |Определяет x-координату центра вращения текстового блока относительно начала фигуры. Формула по умолчанию: = \* Ширина 0,5  <br/> |[TxtPinX Cell (Text Transform Section)](txtpinx-cell-text-transform-section.md) <br/> |
|TxtPinY  <br/> |Определяет координату Y центра вращения текстового блока относительно начала фигуры. Формула по умолчанию: = Height \* 0.5  <br/> |[TxtPinY Cell (Text Transform Section)](txtpiny-cell-text-transform-section.md) <br/> |
|TxtWidth  <br/> |Определяет ширину текстового блока. Формула по умолчанию: = Ширина \* 1  <br/> |[TxtWidth Cell (Text Transform Section)](txtwidth-cell-text-transform-section.md) <br/> |
|UIVisibility  <br/> |Определяет, будет ли имя страницы открыно в пользовательском интерфейсе.  <br/> |[UIVisibility Cell (Page Properties Section)](uivisibility-cell-page-properties-section.md) <br/> |
|UpdateAlignBox  <br/> |Пересчитывание прямоугольника выбора при перемещении работки управления.  <br/> |[UpdateAlignBox Cell (Miscellaneous Section)](updatealignbox-cell-miscellaneous-section.md) <br/> |
|UseGroupGradient  <br/> |Определяет, принимает ли фигура градиент, если фигура сгруппирована вместе с другими фигурами в качестве boolean. Значение ячейки UseGroupGradient влияет только на заливку фигуры.  <br/> |[UseGroupGradient Cell (Gradient Properties Section)](usegroupgradient-cell-gradient-properties-section.md) <br/> |
|VariationColorIndex  <br/> |Определяет индекс цвета активного варианта темы на странице в качестве integer.  <br/> |[VariationColorIndex Cell (Theme Properties Section)](variationcolorindex-cell-theme-properties-section.md) <br/> |
|VariationStyleIndex  <br/> |Определяет индекс стиля активного варианта темы на странице в качестве integer.  <br/> |[VariationStyleIndex Cell (Theme Properties Section)](variationstyleindex-cell-theme-properties-section.md) <br/> |
|VerticalAlign  <br/> |Определяет вертикальное выравнивание текста в текстовом блоке.  <br/> |[VerticalAlign Cell (Text Block Format Section)](verticalalign-cell-text-block-format-section.md) <br/> |
|ViewMarkup  <br/> |Определяет, отображается ли разметка в окне рисования.  <br/> |[ViewMarkup Cell (Document Properties Section)](viewmarkup-cell-document-properties-section.md) <br/> |
|WalkPreference  <br/> |Определяет, перемещается ли конечная точка 1-D-фигуры в горизонтальную или вертикальную точку подключения к фигуре, к какой фигуре она приглушена, с помощью динамического приклейки, когда фигура перемещается в неоднозначное положение. По умолчанию обе конечные точки размерной фигуры перемещаются в горизонтальные точки подключения.  <br/> |[WalkPreference Cell (Glue Info Section)](walkpreference-cell-glue-info-section.md) <br/> |
|Width  <br/> |Содержит ширину выбранной фигуры в единицах рисования. Формула по умолчанию для определения ширины 1-D фигуры: = SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)  <br/> |[Width Cell (Shape Transform Section)](width-cell-shape-transform-section.md) <br/> |
|XGridDensity  <br/> |Указывает тип горизонтальной сетки для использования.  <br/> |[Ячейка XGridDensity (раздел &amp; "Линейка сетки")](xgriddensity-cell-rulergrid-section.md) <br/> |
|XGridOrigin  <br/> |Указывает горизонтальную координату начала сетки.  <br/> |[Ячейка XGridOrigin (раздел &amp; "Сетка линейки")](xgridorigin-cell-rulergrid-section.md) <br/> |
|XGridSpacing  <br/> |Определяет расстояние между горизонтальными линиями в фиксированной сетке (XGridDensity = 0).  <br/> |[Ячейка XGridSpacing (раздел &amp; "Сетка линейки")](xgridspacing-cell-rulergrid-section.md) <br/> |
|XRulerDensity  <br/> |Определяет горизонтальные промежуточные деления линейки для страницы.  <br/> |[Ячейка XRulerDensity (раздел &amp; "Сетка линейки")](xrulerdensity-cell-rulergrid-section.md) <br/> |
|XRulerOrigin  <br/> |Указывает точку начала координат на линейке по оси X для страницы.  <br/> |[Ячейка XRulerOrigin (раздел &amp; "Сетка линейки")](xrulerorigin-cell-rulergrid-section.md) <br/> |
|YGridDensity  <br/> |Указывает тип вертикальной сетки для использования.  <br/> |[YGridDensity Cell (Ruler &amp; Grid Section)](ygriddensity-cell-rulergrid-section.md) <br/> |
|YGridOrigin  <br/> |Указывает начало сетки по вертикали.  <br/> |[YGridOrigin Cell (Ruler &amp; Grid Section)](ygridorigin-cell-rulergrid-section.md) <br/> |
|YGridSpacing  <br/> |Определяет расстояние между вертикальными линиями в фиксированной сетке (YGridDensity = 0).  <br/> |[YGridSpacing Cell (Ruler &amp; Grid Section)](ygridspacing-cell-rulergrid-section.md) <br/> |
|YRulerDensity  <br/> |Определяет вертикальные промежуточные деления линейки для страницы.  <br/> |[Ячейка YRulerDensity (раздел &amp; "Линейка сетки")](yrulerdensity-cell-rulergrid-section.md) <br/> |
|YRulerOrigin  <br/> |Указывает точку начала координат на линейке по оси y для страницы.  <br/> |[Ячейка YRulerOrigin (раздел &amp; "Линейка сетки")](yrulerorigin-cell-rulergrid-section.md) <br/> |
   

