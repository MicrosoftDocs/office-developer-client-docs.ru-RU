---
title: Интерфейсы поле диалоговое окно быстрого хранения (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: В этом разделе описываются интерфейсы, которые можно использовать для задания программным путем диалоговое окно быстрого контроля над заполнением записей в OneNote 2013.
ms.openlocfilehash: d2647ed4d7b9f4487c033260eba8df1e4281c6ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807669"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Интерфейсы поле диалоговое окно быстрого хранения (OneNote)

В этом разделе описываются интерфейсы, которые можно использовать для задания программным путем диалоговое окно быстрого контроля над заполнением записей в OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Диалоговое окно Быстрая подготовка файлов

Диалоговое окно быстрого контроля над заполнением записей в OneNote 2013 — это настраиваемое диалоговое окно, которое позволяет пользователям выбирать расположение в структуре иерархии OneNote. Доступно для выбора расположения включают записные книжки, групп разделов, разделы, страницы и вложенные страницы. Диалоговое окно используется как в приложении OneNote, так и с внешних приложений с помощью API-интерфейса OneNote 2013. На рисунке 1 показано диалоговое окно быстрого контроля над заполнением записей в состояние по умолчанию.
  
**На рисунке 1. Быстрый диалоговое окно хранения без настройки**

![Быстрый контроля над заполнением записей диалоговое окно без настройки] (media/ON15Con_quick_filing_dialog.jpg "Быстрый контроля над заполнением записей диалоговое окно без настройки")
  
В диалоговом окне пользователи могут переходить иерархии всех записных книжек искать определенные расположения или поиска в древовидной структуре OneNote, введя в текстовом поле. Заголовок, описание, список последних результатов, флажок текст и состояний, глубина вложенности, кнопок и типов доступно для выбора размещения следующие аспекты диалогового окна, который можно настроить.

Можно получить доступ к функциональности диалогового окна быстрого контроля над заполнением записей через два интерфейса OneNote 2013. Интерфейс **IQuickFilingDialog** позволяет пользователям создать, настроить и запустить диалоговое окно. Интерфейс **IQuickFilingDialogCallback** вызывается после диалоговое окно закрывается. Запустите окно в процессе OneNote, чтобы механизм необходимо хранить потоке, диалоговое окно "" и затем запись Выбор пользователя и состояние диалогового окна при ее закрытии. 
  
## <a name="iquickfilingdialog-interface"></a>Интерфейс IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Этот интерфейс позволяет пользователю настраивать и запустите диалоговое окно. Пользователя можно создать экземпляр диалоговое окно с помощью класса **приложения** с помощью метода **Application.QuickFilingDialog** . Метод возвращает экземпляр диалогового окна. После задания свойств диалоговое окно метод **IQuickFilingDialog.Run** используется для запуска диалоговое окно. Этот метод запускает диалоговое окно в новом потоке. 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Название** <br/> |string  <br/> |Получает или задает текст заголовка, который отображается в строке заголовка диалогового окна.  <br/> |
|**Описание** <br/> |string  <br/> |Получает или задает текстовое описание, чтобы указать пользователя о том, что для выбора. Это значение может быть несколько строк текста.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Получает или задает текст, который следует за этот флажок. Если задано это значение к типу string непустые флажок отображается в диалоговом окне. Если значение равно пустой строке, отсутствуют не будет.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Получает или задает состояние флажка. Если значение задано значение **false**, этот флажок снят, при запуске диалоговое окно. Если значение задано значение **true**, флажок при запуске, пока **CheckboxText** — это строка непустые диалоговое окно.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Получает идентификатор дескриптор быстрого контроля над заполнением записей диалогового окна.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Получает или задает глубину дерева OneNote должно отображаться в разделе всех записных книжек. По умолчанию отображается дерево до раздела. Это свойство не влияет на элементы какого типа может быть выбран.  <br/> Если элемент **TreeDepth** ниже в иерархии OneNote не может быть выбран по любой из кнопок, глубина отображаемого дерева будет наименьший возможный элемент доступно для выбора. То есть если глубина вложенности настроен для отображения вниз до страниц, но низший доступно для выбора элемента посвящен отдельный раздел, вниз до раздела отображения дерева.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Получает или задает код дескриптора родительского окна диалогового окна. Если задано это свойство, диалоговое окно быстрого контроля над заполнением записей будет модальное назначенный родительского окна при открытии диалогового окна. То есть пользователь, не сможет получить доступ к родительского окна до закрытия диалоговое окно быстрого контроля над заполнением записей.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Получает или задает позицию окна, при использовании экрана. По умолчанию диалоговое окно отображается в центре родительского окна или с рабочего стола.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Получает идентификатор объекта расположения OneNote, выбранный пользователем, когда диалоговое окно закрывается. При нажатии кнопки **Отмена** объекта задано значение null.  <br/> |
|**PressedButton** <br/> |ulong  <br/> |Получает, какая кнопка была нажата при закрытии диалоговое окно. Если была нажата кнопка **Отмена** , данное свойство возвращает значение -1. Все другие кнопки присваиваются значения целое число от 0, увеличивается на 1 для каждого кнопка, добавленная в диалоговое окно. Целое число от кнопки **ОК** по умолчанию равно 0.  <br/> |
   
### <a name="methods"></a>Методы

**SetRecentResults**

|||
|:-----|:-----|
|**Описание** <br/> |Задает, какой список последних результатов будет отображаться в диалоговом окне быстрого контроля над заполнением записей и указывает, следует ли включать некоторые специальные хранения расположения в списке. Пользователи могут выбрать список последних результатов из перечисления [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) . Пользователи также могут выбрать для добавьте следующие параметры в список: текущий раздел, текущей страницы или раздела. Если выбрано **RecentResultType.rrtNone** , будет показан не список последних результатов.  <br/> |
|**Синтаксис** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Параметры** <br/> | _recentResults_ &ndash; Объект типа **RecentResultType** , которое указывает, какой список последних результатов, если они существуют, должны отображаться. Если выбрано **rrtNone** , не список последних результатов отображается в диалоговом окне.<br/><br/>  _fShowCurrentSection_ &ndash; Логическое значение, указывающее, включены ли текущего раздела в список последних результатов.<br/><br/>  _fShowCurrentPage_ &ndash; Логическое значение, указывающее, включены ли текущей страницы в список последних результатов.<br/><br/>  _fShowUnfiledNotes_ &ndash; Логическое значение, указывающее, включены ли в разделе раздела в список последних результатов.  <br/> |
   
> [!NOTE]
> Невозможно выбрать расположение специальные хранения можно использовать любой из кнопок в диалоговом окне, не отображается в списке. Если не доступно для выбора в списке последние результатов найден элемент, отображается список не последних результатов. 
  
В следующем примере метод **SetRecentResults** используется для отображения текущего раздела, текущей страницы и в разделе раздела в список последних результатов. 
  
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
|**Описание** <br/> |Пользователи могут добавлять и настраивать кнопки в диалоговом окне. Пользователи могут указать текст для кнопок и какие элементы в иерархии OneNote можно выбирать с кнопками.  <br/> |
|**Синтаксис** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Параметры** <br/> | _bstrText_ &ndash; Строку, которая определяет текст, который отображается на кнопке. Чтобы настроить кнопки **ОК** по умолчанию, передайте значение null в качестве **bstrText**.  <br/><br/>_allowedElements_ &ndash; **HierarchyElement** , которое указывает, какие элементы иерархии OneNote не только для чтения пользователь может выбрать с помощью кнопки. Для выбора нескольких элементов, пользователь должен передавать оператор **или** для всех uint эквивалентные значения типов **HierarchyElement** , разрешенных в качестве **HierarchyElement**.<br/><br/>  _allowedReadOnlyElements_ &ndash; **HierarchyElement** , которое указывает, какие элементы иерархии только для чтения OneNote пользователь может выбрать с помощью кнопки. Для выбора нескольких элементов, пользователь должен передавать оператор **или** для всех значений эквивалентами **uint** типов **HierarchyElement** , разрешенных в качестве **HierarchyElement**.<br/><br/>  _fDefault_ &ndash; Логическое значение, указывающее, следует ли эта кнопка кнопкой по умолчанию. Если несколько кнопок устанавливается по умолчанию, последний указанный кнопка становится кнопкой по умолчанию.  <br/> |
   
В следующем примере добавляется три кнопки в диалоговое окно быстрого контроля над заполнением записей. Первый из них, **все**, можно выбрать, все элементы в дереве иерархии OneNote. Другие, **записные книжки** и **страниц**, можно выбрать только в том случае, если выбраны соответствующие элементы, записные книжки и страницы.
  
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
|**Описание** <br/> |Отображает диалоговое окно быстрого контроля над заполнением записей из нового потока. Требуемое ссылку на интерфейс **IQuickFilingDialogCallback** , будет вызван метод которого **OnDialogClosed** после диалоговое окно закрывается.  <br/> |
|**Синтаксис** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Параметры** <br/> | _piCallback_ &ndash; Ссылку на интерфейс **IQuickFilingDialogCallback** , который будет создан после диалоговое окно закрывается.  <br/> |
   
В следующем примере метод **Run** для отображения диалогового окна быстрого контроля над заполнением записей из нового потока. 
  
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
|**Описание** <br/> |Указывает, следует ли разворачивать и сворачивать дерева иерархии.  <br/> |
|**Синтаксис** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Параметры** <br/> | _tcs_ - указывает, будет ли дерево развернут или свернут.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Описание** <br/> |Фильтрация списка записных книжек показано по типу.  <br/> |
|**Синтаксис** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Параметры** <br/> | _nfo_ - указывает набор записные книжки, которые должны быть отфильтрованы из списка  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Описание** <br/> |Отображает записной книжки параметр создать в диалоговом окне.  <br/> |
|**Синтаксис** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Описание** <br/> |Добавляет пользователя как начальное редактора в записной книжке в диалоговом окне быстрого контроля над заполнением записей.  <br/> |
|**Синтаксис** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Параметры** <br/> | _initialEditor_ - адрес электронной почты пользователя, которого вы хотите добавить как редактор в блокноте. При создании записной книжки через диалоговое окно быстрого контроля над заполнением записей, автоматически становятся доступными все начальные редакторы.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Описание** <br/> |Удаляет все начальные редакторы из диалогового окна быстрого контроля над заполнением записей.  <br/> |
|**Синтаксис** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Описание** <br/> |Отображает гиперссылку общего доступа к раздела справки в диалоговом окне быстрого контроля над заполнением записей.  <br/> |
|**Синтаксис** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Параметры** <br/> |Нет  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Интерфейс IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Этот интерфейс позволяет пользователям получать доступ к диалогового окна Свойства поля после диалоговое окно закрывается. После закрытия диалогового окна OneNote 2013 вызывает метод **IQuickFilingDialogCallback.OnDialogClose** в этот интерфейс. 
  
Класс, который наследует этот интерфейс должен быть определен.
  
### <a name="methods"></a>Методы

В следующем разделе описываются методы, связанные с интерфейсов, описанных ранее.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Описание** <br/> |Позволяет пользователям добавлять функциональные возможности захвата и использовать в диалоговом окне Выбор пользователей. Этот метод вызывается после закрытия диалоговое окно быстрого контроля над заполнением записей. Этот метод является функцией, для которого **IQuickFilingDialogCallback** интерфейсы для определения.  <br/> |
|**Синтаксис** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Параметры** <br/> | _диалоговое окно_ &ndash; **IQuickFilingDialog** объекта, который вызвал метод **OnDialogClose** .  <br/> |
   
Следующий пример является интерфейсом **IQuickFilingDialogCallback** образца. Метод **OnDialogClose** печатает Выбор пользователя из диалогового окна быстрого контроля над заполнением записей на консоль. 
  
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

В следующем примере кода открывается быстрого контроля над заполнением записей диалоговое окно, которое содержит настраиваемый заголовок, описание, список последних результатов, глубина вложенности, флажок и кнопки. Пользователя выбранного элемента, нажата кнопка, и состояние флажка будет отображаться в окне консоли, когда диалоговое окно закрывается. Для просмотра кнопки страницы включено, пользователь будет иметь для поиска для страницы и выберите его, так как глубина вложенности задано значение разделах. Диалоговое окно не является дочерним любого окна.
  
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

- [Справочник разработчика по OneNote](onenote-developer-reference.md)

