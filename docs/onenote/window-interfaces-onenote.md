---
title: Интерфейсы window (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Интерфейсы Window и Windows — это объекты API OneNote 2013, которые позволяют пользователям работать с окнами OneNote. Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317039"
---
# <a name="window-interfaces-onenote"></a>Интерфейсы window (OneNote)

Интерфейсы **Window** и **Windows** — это объекты API OneNote 2013, которые позволяют пользователям работать с окнами OneNote. Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон. 
  
## <a name="onenote-window-views"></a>Представления окна OneNote

В следующем списке показаны четыре режима просмотра, которые можно использовать для окон OneNote: 
  
- Обычное представление — отображает окно OneNote по умолчанию, в котором отображаются области навигации "Записная книжка" и "Страница".
    
- Представление "Полная страница" — отображает минимальное представление пользовательского интерфейса, в котором области "Записная книжка" и "Страница" не отображаются.
    
- Краткое примечание. Отображает небольшое окно, которое позволяет пользователям делать короткие заметки. Как правило, доступ к быстрым заметкам можно получить с помощью значка  OneNote в области уведомлений Windows, но вы также можете получить к ним доступ с помощью вкладки "Просмотр" в OneNote. 
    
- Закрепление на рабочем столе — отображает окно OneNote, которое можно пристыковать к любой стороне рабочего стола (аналогично панели задач). Это представление уменьшает размер рабочего стола в зависимости от размера окна. В любое время можно пристыковать только одно окно, и окно всегда отображается, не блокируя рабочий стол. 
    
На следующем рисунке показано, как выглядит представление "Полная страница", "Док-станция до рабочего стола" и краткие заметки на рабочем столе.
  
**Представления OneNote**

![В окне OneNote представления](media/ON15Con_views.jpg "окон OneNote")
  
## <a name="interfaces"></a>Интерфейсы

В этом разделе перечислены интерфейсы и члены, которые можно использовать для изменения Windows OneNote программным путем.
  
### <a name="windows-interface"></a>Интерфейс Windows

Интерфейс **Windows** позволяет пользователю получить доступ к набору открытых окон OneNote. Это свойство класса приложения **OneNote,** доступ к нему можно получить через **Application.Windows.** Возвращается enumerated набор окон OneNote. 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Получает количество объектов **Window** в **наборе Windows.**  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Получает объект **Window** активного окна OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Возвращает объект **Window,** соответствующий переданным значению индекса. Доступ к этому свойству напрямую не перейти. Чтобы вернуть объект **Window,** используйте **windows [(uint) index]**.  <br/> |
   
### <a name="window-interface"></a>Интерфейс окна

Интерфейс **Window** позволяет пользователю получать доступ к определенным свойствам каждого окна. Для доступа к каждому окну OneNote можно использовать свойство **Windows** класса **Application.** 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Получает или задает значение, которое указывает, является ли окно активным окном OneNote.  <br/> |
|**Application** <br/> |**Application** <br/> |Получает объект приложения  OneNote, связанный с окном.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Получает ИД объекта активной страницы OneNote окна.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Получает ИД объекта активного раздела OneNote окна.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Получает ИД объекта активной группы разделов OneNote окна.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Получает ИД объекта активной записной книжки OneNote окна.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Получает или задает закрепленное расположение окна OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Получает или задает значение, которое указывает, находится ли окно в представлении "Полная страница" (минимальное представление пользовательского интерфейса).  <br/> |
|**SideNote** <br/> |bool  <br/> |Получает или задает значение, которое указывает, является ли окно окном с кратким примечанием.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Получает ИД работки окна OneNote.  <br/> |
   
**Методы**
  
Для навигации по указанным объектам в окне OneNote или по указанным URL-адресам можно использовать следующие методы интерфейса **Window.** 
  
**NavigateTo**

|||
|:-----|:-----|
|**Описание** <br/> |Переход к указанному объекту в окне OneNote. Например, можно перейти к разделам, страницам и элементам структур на страницах.  <br/> |
|**Синтаксис** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Параметры** <br/> | _bstrHierarchyObjectID_— ид иерархии OneNote объекта, к который нужно перейти. ИД объекта может ссылаться на записную книжку, раздел, группу разделов или страницу OneNote.  <br/>  _bstrObjectID_— ИД OneNote конкретного объекта для перемещения на страницу OneNote. Если пользователь не хочет переходить к определенному объекту на странице, этому параметру задано null.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Описание** <br/> |Если передана ссылка OneNote (onenote://), откроется окно OneNote для соответствующего расположения в OneNote. Однако если ссылка является внешней ссылкой, например https:// или file://, появится диалоговое окно безопасности. После этого OneNote пытается открыть ссылку, и возвращается ошибка HResult.hrObjectDoesNotExist.  <br/> |
|**Синтаксис** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Параметры** <br/> | _bstrUrl_— URL-адрес для навигации.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Описание** <br/> |Пристыковка окна к расположению, указанному **dockLocation** и монитором **в ptMonitor.**  <br/> |
|**Синтаксис** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Параметры** <br/> | _dockLocation_ — указывает закрепленное расположение окна OneNote 2013.  <br/>  _ptMonitor_ ( Необязательный) — указывает в координатах x,y, на которые следует пристыковать окно.  <br/> |
   
## <a name="example"></a>Пример

Следующий код проходит через окна OneNote, чтобы найти закрепленное окно. Если закрепленное окно не существует, пример пристыковит активное окно. Если активного окна нет, код создает новое закрепленное окно.
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a>См. также

- [Справочник разработчика для OneNote](onenote-developer-reference.md)

