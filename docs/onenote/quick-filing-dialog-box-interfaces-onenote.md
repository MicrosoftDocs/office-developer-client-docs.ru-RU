---
title: Интерфейсы диалоговых окне "Быстрая подача данных" (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: В этом разделе описываются интерфейсы, которые можно использовать для программной настройки диалоговых окна "Быстрая подача данных" в OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425339"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Интерфейсы диалоговых окне "Быстрая подача данных" (OneNote)

В этом разделе описываются интерфейсы, которые можно использовать для программной настройки диалоговых окна "Быстрая подача данных" в OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Диалоговое окно "Быстрая подача документов"

Диалоговое окно "Быстрая подача данных" в OneNote 2013 — это настраиваемое диалоговое окно, которое позволяет пользователям выбирать расположение в структуре иерархии OneNote. К выбранным расположениям относятся записные книжки, группы разделов, разделы, страницы и подпапки. Диалоговое окно используется как в приложении OneNote, так и во внешних приложениях с помощью API OneNote 2013. На рисунке 1 показано диалоговое окно "Быстрая подача" в состоянии по умолчанию.
  
**Рисунок 1. Диалоговое окно "Быстрая подача документов" без настроек**

![Диалоговое окно "Быстрая подача документов"]без настройки диалоговое окно "Быстрая подача(media/ON15Con_quick_filing_dialog.jpg "документов\" без настроек")
  
В диалоговом окне пользователи могут перейти по иерархии "Все записные книжки", чтобы найти определенные расположения, или найти структуру дерева OneNote, введя текстовое поле. Параметры диалогового окна, которые можно настроить, включают название, описание, список последних результатов, текст и состояние в поле, глубину дерева, кнопки и типы выбора расположения.

Доступ к диалоговом окну "Быстрая подача данных" можно получить с помощью двух интерфейсов OneNote 2013. Интерфейс **IQuickFilingDialog** позволяет пользователям создать, настроить и запустить диалоговое окно. Интерфейс **IQuickFilingDialogCallback** будет вызван после закрытия диалоговых окно. Диалоговое окно запущено в процессе OneNote, поэтому требуется механизм для поддержания потока диалоговых окна, а затем для записи выбора пользователя и состояния диалоговое окно при закрытии. 
  
## <a name="iquickfilingdialog-interface"></a>Интерфейс IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Этот интерфейс позволяет пользователю настраивать и запускать диалоговое окно. Пользователь может с помощью метода **Application.QuickFilingDialog** сделать диалоговое окно с помощью класса Application.  Метод возвращает экземпляр диалоговых окно. После того как свойства диалоговых окна задаются, для запуска диалоговых окно используется метод **IQuickFilingDialog.Run.** Этот метод запускает диалоговое окно в новом потоке. 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Получает или задает текст заголовка, который отображается в заголовке окна диалогового окна.  <br/> |
|**Описание** <br/> |string  <br/> |Получает или задает текстовое описание, указывав пользователю, что выбрать. Это значение может быть многострочная строка текста.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Получает или задает текст, который следует за этим полем. Если для этого значения установлена непустая строка, в диалоговом окне появится этот диалоговое окно. Если значением является пустая строка, никакие из них не появляются.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Возвращает или задает состояние этого контрольного окна. Если за установлено значение **false,** то при нарабатыии диалоговом окне этот установлен. Если установлено значение **true,** то при входящих в диалоговое окно диалоговых окнах устанавливается непустая строка **checkboxText.**  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Получает ИД работки диалогового окна "Быстрая подача документов".  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Получает или задает глубину отображения дерева OneNote в разделе "Все записные книжки". По умолчанию дерево отображается до разделов. Это свойство не влияет на тип элементов, которые можно выбрать.  <br/> Если в иерархии OneNote установлен элемент **TreeDepth,** который находится ниже, чем может быть выбран любой из кнопок, отображаемая глубина дерева будет самым низким из возможных элементов, которые можно выбрать. То есть, если глубина дерева настроена на отображение вниз по страницам, но самый низкий из выбираемых элементов — это раздел, дерево отображается вниз до разделов.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Получает или задает ИД работки родительского окна диалоговых окон. Если это свойство установлено, диалоговое окно "Быстрая подача документов" будет модальным для назначенного родительского окна, когда откроется диалоговое окно. То есть пользователь не сможет получить доступ к родительскому окну, пока диалоговое окно "Быстрая подача данных" не будет закрыто.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Получает или задает положение окна относительно экрана. По умолчанию диалоговое окно отображается в центре родительского окна или рабочего стола.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Получает ИД объекта расположения OneNote, выбранного пользователем при закрытии диалоговых окно. Если пользователь нажимает кнопку **"Отмена",** для объекта устанавливается null.  <br/> |
|**PressedButton** <br/> |ulong  <br/> |Получает, какая кнопка была нажата при закрытии диалоговое окно. Если **кнопка** "Отмена" была нажата, это свойство возвращает значение -1. Всем другим кнопкам назначены значения от 0 до 1 для каждой кнопки, добавленной в диалоговое окно. Для кнопки "ОК"  по умолчанию имеется значение 0.  <br/> |
   
### <a name="methods"></a>Methods

**SetRecentResults**

|||
|:-----|:-----|
|**Описание** <br/> |Задает список последних результатов, который будет отображаться в диалоговом окне "Быстрая подача документов", и указывает, следует ли включить в список некоторые специальные расположения для хранения. Пользователи могут выбрать список последних результатов из списка [RecentResultType.](enumerations-onenote-developer-reference.md#odc_RecentResultType) Пользователи также могут добавить в список следующие параметры: "Текущий раздел", "Текущая страница" или "Невыверченные заметки". Если **выбран RecentResultType.rrtNone,** список последних результатов не отображается.  <br/> |
|**Синтаксис** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Параметры** <br/> | _recentResults_ &ndash; Объект типа **RecentResultType,** который указывает, какой последний список результатов должен отображаться, если таковый имеется. Если **выбрано rrtNone,** в диалоговом окне не отображается список последних результатов.<br/><br/>  _fShowCurrentSection_ &ndash; Boolean value that indicates whether the current section should be included in the recent result list.<br/><br/>  _fShowCurrentPage_ &ndash; Boolean value that indicates whether the current page should be included in the recent result list.<br/><br/>  _fShowUnfiledNotes_ &ndash; Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.  <br/> |
   
> [!NOTE]
> Если специальное расположение для хранения невозможно выбрать с помощью кнопок в диалоговом окне, оно не отображается в списке. Если в списке последних результатов не найдено ни элемента, ни один из последних результатов не отображается. 
  
В следующем примере метод **SetRecentResults** используется для отображения текущего раздела, текущей страницы и раздела "Unfiled Notes" в списке последних результатов. 
  
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
|**Описание** <br/> |Позволяет пользователям добавлять и настраивать кнопки в диалоговом окне. Пользователи могут указать текст на кнопках и элементы иерархии OneNote, которые могут быть выбраны каждой кнопкой.  <br/> |
|**Синтаксис** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Параметры** <br/> | _bstrText_ &ndash; Строка, указывавая текст, который должен отображаться на кнопке. Чтобы настроить кнопку **"ОК"** по умолчанию, передав значение null **в качестве bstrText.**  <br/><br/>_allowedElements_ &ndash; **Элемент HierarchyElement,** который указывает, какие элементы иерархии OneNote, не только для чтения, пользователь может выбрать с помощью кнопки. При выборе нескольких элементов пользователь должен передать оператор **OR** для всех эквивалентных значений uint типов **HierarchyElement,** разрешенных в качестве **HierarchyElement.**<br/><br/>  _allowedReadOnlyElements_ &ndash; **Элемент HierarchyElement,** который указывает, какие элементы иерархии OneNote разрешено выбирать пользователю с помощью кнопки. При выборе нескольких элементов пользователь должен передать оператор **OR** для всех значений **uint-эквивалентов** типов **HierarchyElement,** разрешенных в качестве **HierarchyElement.**<br/><br/>  _fDefault_ &ndash; Boolean value that specifies whether this button should be the default button. Если несколько кнопок заданы по умолчанию, последняя указанная кнопка становится кнопкой по умолчанию.  <br/> |
   
В следующем примере в диалоговое окно "Быстрая подача документов" добавляются три кнопки. Первый элемент( **All)** может быть выбран всеми элементами в дереве иерархии OneNote. Остальные **записные книжки** и страницы можно выбрать, только если выбраны соответствующие элементы, записные книжки и страницы. 
  
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
|**Описание** <br/> |Отображает диалоговое окно "Быстрая подача документов" из нового потока. Он принимает ссылку на интерфейс **IQuickFilingDialogCallback,** метод **OnDialogClosed** которого будет вызван после закрытия диалоговое окно.  <br/> |
|**Синтаксис** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Параметры** <br/> | _piCallback_ &ndash; Ссылка на интерфейс **IQuickFilingDialogCallback,** который будет созважен после закрытия диалоговых окном.  <br/> |
   
В следующем примере метод **Run** используется для отображения диалоговых окна "Быстрая подача" из нового потока. 
  
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
|**Описание** <br/> |Указывает, следует ли развернуть или свернуть дерево иерархии.  <br/> |
|**Синтаксис** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Параметры** <br/> | _tcs_ — указывает, будет ли дерево расширено или свернуто.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Описание** <br/> |Фильтрует список записных книжок, показанных по типу.  <br/> |
|**Синтаксис** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Параметры** <br/> | _nfo_ — указывает набор записных книзок, которые необходимо отфильтровать из списка  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Описание** <br/> |Отображает параметр создания записной книжки в диалоговом оке.  <br/> |
|**Синтаксис** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Описание** <br/> |Добавляет пользователя в качестве начального редактора в записную книжку в диалоговом окне "Быстрая подача данных".  <br/> |
|**Синтаксис** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Параметры** <br/> | _initialEditor_ — адрес электронной почты пользователя, который вы хотите добавить в записную книжку в качестве редактора. Когда записная книжка создается в диалоговом окне "Быстрая подача документов", она автоматически передается всем начальным редакторам.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Описание** <br/> |Удаляет все начальные редакторы из диалогового окна "Быстрая подача документов".  <br/> |
|**Синтаксис** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Описание** <br/> |Отображает гиперссылку раздела справки по совместному доступу в диалоговом окне "Быстрая подача документов".  <br/> |
|**Синтаксис** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Интерфейс IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Этот интерфейс позволяет пользователю получать доступ к свойствам диалоговых окно после закрытия диалоговых окно. После закрытия диалоговое окно OneNote 2013 вызывает метод **IQuickFilingDialogCallback.OnDialogClose** в этом интерфейсе. 
  
Необходимо определить класс, наследуемый этим интерфейсом.
  
### <a name="methods"></a>Methods

В следующем разделе описаны методы, связанные с интерфейсами, которые были подробно описаны ранее.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Описание** <br/> |Позволяет пользователям добавлять функции для захвата и использования выбора пользователя в диалоговом окне. Этот метод будет вызван после закрытия диалоговых окна "Быстрая подача документов". Этот метод является функцией, которую должны определять интерфейсы **IQuickFilingDialogCallback.**  <br/> |
|**Синтаксис** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Параметры** <br/> | _диалоговое окно_ &ndash; Объект **IQuickFilingDialog,** который вызвал **метод OnDialogClose.**  <br/> |
   
Ниже приводится пример интерфейса **IQuickFilingDialogCallback.** Метод **OnDialogClose** печатает выбор пользователя в диалоговом окне "Быстрая подача данных" на консоль. 
  
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

В следующем примере кода открывается диалоговое окно "Быстрая подача" с настроенным заголовком, описанием, недавним списком результатов, глубиной дерева, полем и кнопками. Выбранный пользователем элемент, нажатая кнопка и состояние проверки будут отображаться в окне консоли при закрытии диалоговых окон. Чтобы увидеть, что кнопка страницы включена, пользователю необходимо будет найти страницу и выбрать ее, так как глубина дерева настроена на разделы. Диалоговое окно не является относячным к любому окну.
  
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

