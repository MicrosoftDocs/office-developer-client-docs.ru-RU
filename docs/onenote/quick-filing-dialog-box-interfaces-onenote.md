---
title: Интерфейсы диалоговых полей quick Filing (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: В этом разделе описываются интерфейсы, которые можно использовать для программной настройки диалоговых окне быстрого заполнения в OneNote 2013 г.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425339"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Интерфейсы диалоговых полей quick Filing (OneNote)

В этом разделе описываются интерфейсы, которые можно использовать для программной настройки диалоговых окне быстрого заполнения в OneNote 2013 г.
  
## <a name="quick-filing-dialog-box"></a>Диалоговое окно Quick Filing

Диалоговое окно Quick Filing в OneNote 2013 г. — настраиваемый диалоговое окно, которое позволяет пользователям выбирать местоположение в OneNote иерархии. Выбранные расположения включают записные книжки, группы разделов, разделы, страницы и подстраховки. Диалоговое окно используется как в приложении OneNote, так и в внешних приложениях через API 2013 OneNote 2013 года. На рисунке 1 показан диалоговое окно Quick Filing в состоянии по умолчанию.
  
**Рис. 1. Диалоговое окно Quick Filing без настроек**

![Диалоговое окно Quick Filing без настроек]диалоговое окно(media/ON15Con_quick_filing_dialog.jpg "Quick Filing без настроек")
  
В диалоговом окне пользователи могут перемещаться по иерархии "Все записные книжки", чтобы найти определенные расположения или OneNote структуру дерева, введя текстовое поле. К числу аспектов диалогового окна, которые можно настроить, относятся название, описание, список результатов последнего времени, текст и состояние окна, глубина дерева, кнопки и выбранные типы расположения.

Вы можете получить доступ к функции диалогового окна быстрой подачи с помощью двух интерфейсов OneNote 2013 года. Интерфейс **IQuickFilingDialog** позволяет пользователям мгновенно, настроить и запустить диалоговое окно. Интерфейс **IQuickFilingDialogCallback** вызван после закрытия диалоговое окно. Диалоговое окно запущено в процессе OneNote, поэтому необходим механизм, чтобы сохранить поток диалоговой точки, а затем зафиксировать выбор пользователя и состояние диалоговой точки при ее закрытии. 
  
## <a name="iquickfilingdialog-interface"></a>Интерфейс IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Этот интерфейс позволяет пользователю настраивать и запускать диалоговое окно. С помощью метода **Application.QuickFilingDialog** пользователь может мгновенно использовать диалоговое окно через класс Application.  Метод возвращает экземпляр диалогового окна. После набора свойств диалоговое окно используется метод **IQuickFilingDialog.Run** для запуска диалогового окна. Этот метод запускает диалоговое окно на новом потоке. 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Получает или задает текст заголовка, который отображается в панели заголовков окна диалогового окна.  <br/> |
|**Описание** <br/> |string  <br/> |Получает или задает текстовое описание, чтобы поручить пользователю, что выбрать. Это значение может быть текстом с несколькими строками.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Получает или задает текст, который следует за чек-полем. Если это значение заданной для непустой строки, в диалоговом окне появится чековое окно. Если значение — пустая строка, не отображается поле.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Получает или задает состояние контрольного окна. Если значение заведомо **ложное,** при окне диалоговое окно будет очищено. Если значение забито на значение **true,** то для начала диалогового окна будет выбрано значение **CheckboxText,** если это непустая строка.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Получает ID ручки окна диалоговое окно быстрой подачи.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Получает или задает глубину OneNote дерева в разделе Все записные книжки. По умолчанию дерево отображается до разделов. Это свойство не влияет на тип элементов, которые можно выбрать.  <br/> Если в иерархии OneNote значение **TreeDepth** ниже, чем может быть выбрано любой из кнопок, отображаемая глубина дерева будет наименьшим из возможных выбранных элементов. То есть, если глубина дерева отображается до страниц, но самый низкий выбранный элемент — это раздел, дерево отображается до разделов.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Получает или задает ID ручки родительского окна диалоговое окно. Если это свойство заданной, диалоговое окно Quick Filing будет модальным для назначенного родительского окна при открываемом диалоговом окне. То есть пользователь не сможет получить доступ к родительскому окну, пока не будет закрыт диалоговое окно "Быстрая подача".  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Получает или задает положение окна по отношению к экрану. По умолчанию диалоговое окно отображается в центре родительского окна или на рабочем столе.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Получает объект ID расположения OneNote, выбранного пользователем при закрытии диалоговое окно. Если пользователь нажмет кнопку **Отмена,** объект будет настроен на нуль.  <br/> |
|**PressedButton** <br/> |ulong  <br/> |Получает, какая кнопка была нажата при закрытии диалоговое окно. Если **кнопка Отмена** была нажата, это свойство возвращает значение -1. Всем другим кнопкам назначены значения из 0, прибавка по 1 для каждой кнопки, добавленной в диалоговое окно. По умолчанию значение кнопки **OK по** умолчанию — 0.  <br/> |
   
### <a name="methods"></a>Методы

**SetRecentResults**

|||
|:-----|:-----|
|**Описание** <br/> |Задает список последних результатов, который будет отображаться в диалоговом окне Быстрая подача, и указывает, следует ли включать в список некоторые специальные расположения для подачи. Пользователи могут выбрать недавний список результатов из списка [RecentResultType.](enumerations-onenote-developer-reference.md#odc_RecentResultType) Пользователи также могут добавить в список следующие параметры: Current Section, Current Page или Unfiled Notes. Если **выбран RecentResultType.rrtNone,** не отображается список результатов.  <br/> |
|**Синтаксис** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Параметры** <br/> | _recentResults_ &ndash; Объект типа **RecentResultType,** который указывает, какой последний список результатов, если таковый имеется, должен отображаться. Если **выбран rrtNone,** в диалоговом окне не отображается последний список результатов.<br/><br/>  _fShowCurrentSection_ &ndash; Значение Boolean, которое указывает, следует ли включить текущий раздел в недавний список результатов.<br/><br/>  _fShowCurrentPage_ &ndash; Значение Boolean, которое указывает, должна ли текущая страница быть включена в недавний список результатов.<br/><br/>  _fShowUnfiledNotes_ &ndash; Значение Boolean, которое указывает, следует ли включить раздел Unfiled Notes в недавний список результатов.  <br/> |
   
> [!NOTE]
> Если специальное расположение подачи невозможно выбрать с помощью кнопок в диалоговом окне, оно не отображается в списке. Если в списке последних результатов не обнаружено выбранного элемента, не отображается недавний список результатов. 
  
В следующем примере метод **SetRecentResults** отображает текущий раздел, текущую страницу и раздел Unfiled Notes в недавнем списке результатов. 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

**AddButton**

|||
|:-----|:-----|
|**Описание** <br/> |Позволяет пользователям добавлять и настраивать кнопки в диалоговом окне. Пользователи могут указать текст на кнопках и какие элементы иерархии OneNote могут быть выбраны каждой кнопкой.  <br/> |
|**Синтаксис** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Параметры** <br/> | _bstrText_ &ndash; Строка, которая указывает текст, который должен отображаться на кнопке. Чтобы настроить кнопку **OK по** умолчанию, передай значение null как **bstrText.**  <br/><br/>_allowedElements_ &ndash; **ИерархияElement,** которая указывает, какие элементы иерархии, не OneNote только для чтения, пользователь может выбрать с помощью кнопки. Для выбора нескольких элементов пользователь должен передать **оператору OR** все эквивалентные значения типов **HierarchyElement,** разрешенные в качестве **HierarchyElement.**<br/><br/>  _allowedReadOnlyElements_ &ndash; **ИерархияElement,** которая указывает, OneNote элементов иерархии только для чтения пользователь может выбрать с помощью кнопки. Для выбора нескольких элементов пользователь должен передать **оператору OR** все значения **uint-эквивалентов** типов **HierarchyElement,** разрешенных как **HierarchyElement.**<br/><br/>  _fDefault_ &ndash; Значение Boolean, которое указывает, должна ли эта кнопка быть кнопкой по умолчанию. Если несколько кнопок заданы по умолчанию, последняя указанная кнопка становится кнопкой по умолчанию.  <br/> |
   
В следующем примере в диалоговом окне Быстрая подача добавляется три кнопки. Первый, **All**, может быть выбран всеми элементами в дереве OneNote иерархии. Остальные **записные книжки** и **страницы** можно выбрать только в том случае, если будут выбраны соответствующие элементы, записные книжки и страницы.
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

**Run**

|||
|:-----|:-----|
|**Описание** <br/> |Отображает диалоговое окно Быстрая подача из нового потока. Он принимает ссылку на **интерфейс IQuickFilingDialogCallback,** метод **onDialogClosed** которого будет вызван после закрытия диалоговое окно.  <br/> |
|**Синтаксис** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Параметры** <br/> | _piCallback_ &ndash; Ссылка на интерфейс **IQuickFilingDialogCallback,** который будет мгновенным после закрытия диалоговое окно.  <br/> |
   
В следующем примере метод **Run** отображает диалоговое окно Quick Filing из нового потока. 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

**TreeCollapsedState**

|||
|:-----|:-----|
|**Описание** <br/> |Указывает, следует ли расширять или свернуть дерево иерархии.  <br/> |
|**Синтаксис** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Параметры** <br/> | _tcs_ — указывает, расширено или рухнуло дерево.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Описание** <br/> |Фильтрует список записных книжк, показанных по типу.  <br/> |
|**Синтаксис** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Параметры** <br/> | _nfo_ — указывает набор записных книжк, которые необходимо отфильтровать из списка  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Описание** <br/> |Отображает новый параметр записной книжки в диалоговом окантовке.  <br/> |
|**Синтаксис** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Описание** <br/> |Добавляет пользователя в качестве начального редактора в записную книжку в диалоговом окне Быстрая подача.  <br/> |
|**Синтаксис** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Параметры** <br/> | _initialEditor_ — адрес электронной почты пользователя, который вы хотите добавить в качестве редактора в блокнот. Когда записная книжка создается в диалоговом окне Быстрая подача, она автоматически передается всем начальным редакторам.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Описание** <br/> |Удаляет все начальные редакторы из диалогового окна "Быстрая подача".  <br/> |
|**Синтаксис** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Описание** <br/> |Отображает гиперссылку раздел справки общего доступа в диалоговом окне Быстрая подача.  <br/> |
|**Синтаксис** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Интерфейс IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Этот интерфейс позволяет пользователю получить доступ к свойствам диалоговых полей после закрытия диалоговое окно. После закрытия диалоговое окно OneNote 2013 вызывает метод **IQuickFilingDialogCallback.OnDialogClose** в этом интерфейсе. 
  
Класс, который наследует этот интерфейс, должен быть определен.
  
### <a name="methods"></a>Методы

В следующем разделе описываются методы, связанные с подробными ранее интерфейсами.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Описание** <br/> |Позволяет пользователям добавлять функции для захвата и использования выбора пользователя из диалогового окна. Этот метод вызван после закрытия диалогового окна "Быстрая подача". Этот метод является функцией, которую должны определить интерфейсы **IQuickFilingDialogCallback.**  <br/> |
|**Синтаксис** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Параметры** <br/> | _диалоговое окно_ &ndash; Объект **IQuickFilingDialog,** который называется **методом OnDialogClose.**  <br/> |
   
Ниже приводится пример **интерфейса IQuickFilingDialogCallback.** Метод **OnDialogClose** печатает выбор пользователя из диалогового окна "Быстрая подача" на консоль. 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a>Пример
<a name="odc_IQuickFilingDialog"> </a>

В следующем примере кода открывается диалоговое окно Quick Filing с настраиваемым названием, описанием, последним списком результатов, глубиной дерева, полем и кнопками. Выбранный элемент пользователя, нажатая кнопка и состояние чек-окна будут отображаться в окне консоли при закрытии диалоговое окно. Чтобы увидеть включенную кнопку страницы, пользователю придется искать страницу и выбирать ее, так как глубина дерева заводится в разделы. Диалоговое окно не является ребенком любого окна.
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a>См. также

- [Справочник разработчика для OneNote](onenote-developer-reference.md)

