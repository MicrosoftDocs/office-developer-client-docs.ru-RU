---
title: Реализация оболочки для инспекторов и отслеживание событий уровня элемента в каждом инспекторе
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a70aedf9a8803a2c990f07a77d4fc730f7263aae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320127"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a>Реализация оболочки для инспекторов и отслеживание событий уровня элемента в каждом инспекторе

Этот раздел содержит два примера кода, показывающие, как реализована оболочка для коллекции [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) и как использовать эту оболочку, чтобы отслеживать события уровня элемента в каждом объекте [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) коллекции.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В следующих двух примерах кода реализованы классы Connect и OutlookInspector. В первом примере кода задействуются методы и обработчики событий, включенные в класс Connect для реализации оболочки коллекции **Inspectors**. Второй пример кода показывает простую реализацию класса **OutlookInspector**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

В представленном ниже примере кода [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) событие возникает после создания нового окна инспектора и перед его отображением. Действием пользователя также можно создать новое окно инспектора. В классе **Connect** объявлена переменная экземпляра уровня класса с именем inspectors, и обрабатывается событие **NewInspector**. 

В методе inspectors\_NewInspector метод **FindOutlookInspector** проверяет, находится ли уже новое окно инспектора в списке inspectorWindows. Если FindOutlookInspector не может найти объект **Inspector** в inspectorWindows, метод **AddInspector** добавляет экземпляр класса **OutlookInspector** в список inspectorWindows. Класс **OutlookInspector** можно использовать, чтобы создать события для этого конкретного окна инспектора. Реализация класса **OutlookInspector** показана во втором примере кода.

```csharp
class Connect
{
    // Connect class-level Instance Variables
    // Outlook inspectors collection
    private Outlook.Inspectors inspectors;

    // Collection of tracked inspector windows              
    private List<OutlookInspector> inspectorWindows;    

    // Hook up NewInspector event
    inspectors.NewInspector += new 
        Outlook.InspectorsEvents_NewInspectorEventHandler(
        inspectors_NewInspector);

    // NewInspector event creates new instance of OutlookInspector
    void inspectors_NewInspector(Outlook.Inspector Inspector)
    {
        // Check to see if this is a new window you don't
        // already track
        OutlookInspector existingWindow = 
            FindOutlookInspector(Inspector);
        if (existingWindow == null)
        {
            AddInspector(Inspector);
        }
    }

    // Adds an instance of **OutlookInspector** class
    private void AddInspector(Outlook.Inspector inspector)
    {
        OutlookInspector window = new OutlookInspector(inspector);
        window.Close +=
            new EventHandler(WrappedInspectorWindow_Close);
    }

    // Looks up the window wrapper for a given Inspector 
    // window object
    private OutlookInspector FindOutlookInspector(object window)
    {
        foreach (OutlookInspector inspector in inspectorWindows)
        {
            if (inspector.Window == window)
            {
                return inspector;
            }
        }
        return null;
    }
}
```

Следующий пример кода является реализацией класса **OutlookInspector**. Этот класс используется, чтобы создавать события для окна инспектора из предыдущего примера кода. Одновременно можно открыть несколько окон инспекторов. События уровня элемента, такие как [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) и [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)), отслеживаются с помощью обработчиков, задаваемых в конструкторе этого класса. Событие [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) для объекта [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) также обрабатывается в конструкторе этого класса. При необходимости можно задать другие переменные экземпляра элемента уровня класса. Все события, обработчики которых подключены в конструкторе OutlookInspector, освобождаются в обработчике события OutlookInspectorWindow\_Close.

Обратите внимание, что на уровне объектной модели объект **Outlook inspector** не относится к какому-либо элементу Outlook. В этом примере кода используется вспомогательный класс OutlookItem, определенный в статье [Создание вспомогательного класса для доступа к распространенным элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), чтобы легко вызывать свойство OutlookItem.Class для проверки класса сообщений текущего элемента в инспекторе до предположения, что элемент является элементом контактов.

```csharp
// This class tracks the state of an Outlook Inspector window 
// and ensures that what happens in this window is handled correctly.
class OutlookInspector
{
    // OutlookInspector class-level instance variables 
    // wrapped window object
    private Outlook.Inspector m_Window;             

    // Use these instance variables to handle item-level events
    // wrapped MailItem
    private Outlook.MailItem m_Mail;    
    // wrapped AppointmentItem        
    private Outlook.AppointmentItem m_Appointment;  
    // wrapped ContactItem
    private Outlook.ContactItem m_Contact;
    // wrapped TaskItem      
    private Outlook.TaskItem m_Task;             

    // OutlookInspector constructor
    public OutlookInspector(Outlook.Inspector inspector)
    {
        m_Window = inspector;

        // Hook up the close event
        ((Outlook.InspectorEvents_Event)inspector).Close +=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Hook up item-level events as needed
        OutlookItem olItem = new OutlookItem(inspector.CurrentItem);
        if(olItem.Class==Outlook.OlObjectClass.olContact)
        {
            m_Contact = olItem.InnerObject as Outlook.ContactItem;
            m_Contact.Open +=
                new Outlook.ItemEvents_10_OpenEventHandler(
                m_Contact_Open);
            m_Contact.PropertyChange +=
                new Outlook.ItemEvents_10_PropertyChangeEventHandler(
                m_Contact_PropertyChange);
            m_Contact.CustomPropertyChange +=
                new Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
                m_Contact_CustomPropertyChange);
        }
    }

    // Event Handler for the inspector close event.
    private void OutlookInspectorWindow_Close()
    {
        // Unhook events from any item-level instance variables
        m_Contact.Open -= 
            Outlook.ItemEvents_10_OpenEventHandler(
            m_Contact_Open);
        m_Contact.PropertyChange -= 
            Outlook.ItemEvents_10_PropertyChangeEventHandler(
            m_Contact_PropertyChange);
        m_Contact.CustomPropertyChange -= 
            Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
            m_Contact_CustomPropertyChange);
        ((Outlook.ItemEvents_Event)m_Contact).Close -= 
            Outlook.ItemEvents_CloseEventHandler(
            m_Contact_Close);

        // Unhook events from the window
        ((Outlook.InspectorEvents_Event)m_Window).Close -=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Raise the OutlookInspector close event
        if (Close != null)
        {
            Close(this, EventArgs.Empty);
        }
        // Release item-level instance variables
        m_Mail = null;
        m_Appointment = null;
        m_Contact = null;
        m_Task = null;
        m_Window = null;
    }
}
```

## <a name="see-also"></a>См. также

- [Примеры задач, в которых используются события Outlook](sample-tasks-using-outlook-events.md)

