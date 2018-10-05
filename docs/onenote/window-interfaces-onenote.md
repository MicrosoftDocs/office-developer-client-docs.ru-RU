---
title: Окно интерфейсы (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Интерфейсы Window и Windows — API-интерфейса OneNote 2013 объекты, позволяющий пользователям для работы с OneNote windows. Эти объекты позволяют пользователям нумерации внутри набора OneNote windows и изменении окно свойств.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399951"
---
# <a name="window-interfaces-onenote"></a>Окно интерфейсы (OneNote)

Интерфейсы **Window** и **Windows** — API-интерфейса OneNote 2013 объекты, позволяющий пользователям для работы с OneNote windows. Эти объекты позволяют пользователям нумерации внутри набора OneNote windows и изменении окно свойств. 
  
## <a name="onenote-window-views"></a>Представления окна OneNote

В следующем списке приведены режимы четыре представления, которые можно использовать для OneNote windows: 
  
- Стандартное представление — отображает окно OneNote по умолчанию, в котором отображаются области переходов записной книжки и страницы.
    
- Полный просмотр страницы — отображает минимальной пользовательского интерфейса (UI) Просмотр в котором области записной книжки и страницы, не отображаются.
    
- Небольшое примечание — отображает небольшое окно, которое позволяет пользователям короткий заметок. Краткие заметки обычно будет доступ через значок OneNote в области уведомлений Windows, но вы также можете открыть их на вкладке **Вид** в OneNote. 
    
- Прикрепить к рабочему столу — отображает окно OneNote, можно закрепить в любой части рабочего стола (аналогично панели задач). В этом представлении уменьшает размер рабочего стола в окно. Только одно окно можно закрепить в любое время и окна всегда видна без блокировки рабочего стола. 
    
На следующем рисунке показаны какие целую страницу представления, закрепления в режим просмотра и памятки иметь вид на рабочем столе.
  
**Представления OneNote**

![Представления окна OneNote] (media/ON15Con_views.jpg "Представления окна OneNote")
  
## <a name="interfaces"></a>Интерфейсы

В этом разделе перечислены интерфейсы и члены, которые можно использовать для изменения OneNote windows программными средствами.
  
### <a name="windows-interface"></a>Интерфейс Windows

Интерфейс **Windows** позволяет пользователям получать доступ к набор открытых окнах OneNote. Это свойство класса OneNote **приложения** , доступ к через **Application.Windows**. При этом будет получен перечисляемые набор OneNote windows. 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Возвращает количество объектов **Window** в наборе **Windows** .  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Возвращает объект **Window** активного окна OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Возвращает объект **Window** , соответствующий переданное значение индекса. Это свойство не может осуществляться непосредственно. Чтобы вернуть объект **Window** , используйте **Windows [(uint) index]**.  <br/> |
   
### <a name="window-interface"></a>Интерфейс окна

Интерфейс **окна** позволяет пользователям получать доступ к определенных свойств каждого окна. Каждое окно OneNote осуществляется путем перечисления через свойство **Windows** класса **приложения** . 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Получает или задает значение, указывающее, является ли окно активным окном OneNote.  <br/> |
|**Приложение** <br/> |**Приложение** <br/> |Получает объект OneNote **приложения** , связанный с окном.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Получает идентификатор объекта активную страницу OneNote окна.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Получает идентификатор объекта разделе OneNote активного окна.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Получает идентификатор объекта группы active OneNote раздела окна.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Получает идентификатор объекта active записной книжки OneNote окна.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Получает или задает расположение закрепленного окна OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Получает или задает значение, указывающее, является ли окно в режиме полного страницы (Минимальная представление пользовательского интерфейса).  <br/> |
|**SideNote** <br/> |bool  <br/> |Получает или задает значение, указывающее, является ли окно окном небольшое примечание.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Получает идентификатор дескриптор окна OneNote.  <br/> |
   
**Методы**
  
Можно использовать следующие методы интерфейса **окна** для перехода для указанных объектов в окне OneNote или для указанного URL-адреса. 
  
**NavigateTo**

|||
|:-----|:-----|
|**Описание** <br/> |Переход на указанный объект в окне OneNote. Например можно перейти к разделов, страницы и элементы структуры в пределах страницы.  <br/> |
|**Синтаксис** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Параметры** <br/> | _bstrHierarchyObjectID_— OneNote идентификатор объекта, чтобы перейти к иерархии. Идентификатор объекта можно ссылаться записной книжки OneNote, раздел, раздел группы или страницы.  <br/>  _bstrObjectID_— OneNote идентификатор для конкретного объекта, чтобы перейти на странице OneNote. Если пользователь не требуется переход к объекту, определенные на странице, этому параметру присвоено значение null.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Описание** <br/> |Если передается ссылка OneNote (onenote: / /), открывается окно OneNote в соответствующем расположении в OneNote. Тем не менее если ссылки внешних ссылок, такие как https:// или file://, появится диалоговое окно безопасности. После увольнение OneNote пытается открыть ссылку и возвращается сообщение об ошибке HResult.hrObjectDoesNotExist.  <br/> |
|**Синтаксис** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Параметры** <br/> | _bstrUrl_— URL-адрес для перехода.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Описание** <br/> |Закрепляет окне местоположение, указанное для монитора на **ptMonitor**и **dockLocation** .  <br/> |
|**Синтаксис** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Параметры** <br/> | _dockLocation_ - указывает расположение закрепленного окна OneNote 2013.  <br/>  _ptMonitor_ - указывает (необязательно) в x, y координаты отслеживающие окна следует закрепить.  <br/> |
   
## <a name="example"></a>Пример

Приведенный ниже код перебирает windows OneNote, чтобы найти закрепленного окна. Если нет закрепленного окна, пример закрепляет активного окна. Если нет активного окна, код создает новый закрепленного окна.
  
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

