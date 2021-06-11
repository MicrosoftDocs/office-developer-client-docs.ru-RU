---
title: Интерфейсы окон (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Интерфейсы Window и Windows являются объектами API 2013 OneNote, которые позволяют пользователям работать с OneNote окнами. Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317039"
---
# <a name="window-interfaces-onenote"></a>Интерфейсы окон (OneNote)

Интерфейсы **Window** **и Windows** являются объектами API 2013 OneNote, что позволяет пользователям работать с OneNote окнами. Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон. 
  
## <a name="onenote-window-views"></a>Представления окна OneNote

В следующем списке показаны четыре режима представления, которые можно использовать для OneNote windows: 
  
- Нормальное представление — отображает окно OneNote, в котором видны области навигации блокнота и страницы.
    
- Полное представление страницы — отображает минимальное представление пользовательского интерфейса (пользовательского интерфейса), в котором не отображаются области блокнота и страницы.
    
- Быстрая заметка— отображает небольшое окно, которое позволяет пользователям делать короткие заметки. Обычно можно получить доступ к быстрым заметкам через значок OneNote в области уведомлений Windows, но вы также можете получить доступ к ним через вкладку **Просмотр** в OneNote. 
    
- Стыковка с настольным компьютером — отображает окно OneNote, которое можно пристыковать к любой стороне рабочего стола (аналогично панели задач). Это представление уменьшает размер рабочего стола, чтобы соответствовать окну. Вы можете состыковать только одно окно в любое время, и окно всегда видно, не блокируя рабочий стол. 
    
На следующем рисунке показано, как выглядит представление "Полная страница", "Стыковка с настольным компьютером" и быстрые заметки на рабочем столе.
  
**Представления OneNote**

![OneNote представления OneNote](media/ON15Con_views.jpg "окна")
  
## <a name="interfaces"></a>Интерфейсы

В этом разделе перечислены интерфейсы и члены, которые можно использовать для программных OneNote Windows.
  
### <a name="windows-interface"></a>Windows интерфейс

Интерфейс **Windows** позволяет пользователю получить доступ к набору открытых OneNote окон. Это свойство класса **OneNote,** доступ к нему через **Application.Windows.** В этом случае возвращается набор OneNote окон. 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Получает число объектов **Window** в **Windows** наборе.  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Получает **объект Window** в окне active OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Возвращает объект **Window,** соответствующий пройденным значениям индекса. Это свойство не может быть напрямую доступны. Чтобы вернуть **объект Window,** **Windows [(uint) index].**  <br/> |
   
### <a name="window-interface"></a>Интерфейс окна

Интерфейс **Window** позволяет пользователю получать доступ к определенным свойствам каждого окна. К OneNote окна можно получить доступ путем Windows **свойства** класса **Application.** 
  
**Свойства**

|**Имя**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Получает или задает значение, которое указывает, является ли окно активным OneNote окном.  <br/> |
|**Application** <br/> |**Application** <br/> |Получает объект OneNote **приложения,** связанный с окном.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Получает объектный ID активной OneNote страницы окна.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Получает объектный ID активного OneNote окна.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Получает объектный ID активной OneNote группы раздела окна.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Получает объектный ID активного OneNote записной книжки окна.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Получает или задает пристыкованное расположение окна OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Получает или задает значение, которое указывает, находится ли окно в представлении full Page (минимальное представление пользовательского интерфейса).  <br/> |
|**SideNote** <br/> |bool  <br/> |Получает или задает значение, которое указывает, является ли окно окном быстрой заметки.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Получает ID ручки окна OneNote.  <br/> |
   
**Методы**
  
Вы можете использовать следующие методы интерфейса **Window** для навигации по указанным объектам в окне OneNote или к указанным URL-адресам. 
  
**NavigateTo**

|||
|:-----|:-----|
|**Описание** <br/> |Переходит к указанному объекту в OneNote окне. Например, можно перейти к разделам, страницам и элементам набросков на страницах.  <br/> |
|**Синтаксис** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Параметры** <br/> | _bstrHierarchyObjectID_— иерархия OneNote ИД объекта, на который необходимо ориентироваться. ID объекта может ссылаться на OneNote, раздел, группу разделов или страницу.  <br/>  _bstrObjectID_— OneNote ID определенного объекта для перемещения в OneNote странице. Если пользователь не хочет переходить к определенному объекту на странице, этот параметр задан как null.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Описание** <br/> |Если передана ссылка OneNote (onenote://), откроется окно OneNote для соответствующего расположения в OneNote. Однако если ссылка является внешней ссылкой, например https:// или file://, появится диалоговое окно безопасности. После увольнения OneNote открыть ссылку и возвращается ошибка HResult.hrObjectDoesNotExist.  <br/> |
|**Синтаксис** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Параметры** <br/> | _bstrUrl_— URL-адрес для навигации.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Описание** <br/> |Пристыковает окно к расположению, указанному **в dockLocation** и монитору **в ptMonitor.**  <br/> |
|**Синтаксис** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Параметры** <br/> | _dockLocation_ — указывает пристыкованное расположение окна OneNote 2013 года.  <br/>  _ptMonitor_ — (необязательный) указывает в x,y координирует, к которому следует пристыковать окно.  <br/> |
   
## <a name="example"></a>Пример

Следующий код итерирует через OneNote, чтобы найти пристыкованное окно. Если не существует пристыкованного окна, в примере пристыковано активное окно. Если нет активного окна, код создает новое пристыкованное окно.
  
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

