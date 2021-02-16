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
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a><span data-ttu-id="48afa-102">Реализация оболочки для инспекторов и отслеживание событий уровня элемента в каждом инспекторе</span><span class="sxs-lookup"><span data-stu-id="48afa-102">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>

<span data-ttu-id="48afa-103">Этот раздел содержит два примера кода, показывающие, как реализована оболочка для коллекции [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) и как использовать эту оболочку, чтобы отслеживать события уровня элемента в каждом объекте [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) коллекции.</span><span class="sxs-lookup"><span data-stu-id="48afa-103">This topic contains two code examples that show how to implement a wrapper for an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) collection and to use that wrapper to track item-level events in each [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) object in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="48afa-104">Пример</span><span class="sxs-lookup"><span data-stu-id="48afa-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="48afa-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="48afa-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="48afa-106">В следующих двух примерах кода реализованы классы Connect и OutlookInspector.</span><span class="sxs-lookup"><span data-stu-id="48afa-106">The following two code examples implement the Connect and OutlookInspector classes.</span></span> <span data-ttu-id="48afa-107">В первом примере кода задействуются методы и обработчики событий, включенные в класс Connect для реализации оболочки коллекции **Inspectors**.</span><span class="sxs-lookup"><span data-stu-id="48afa-107">The first code example involves methods and event handlers you include in the Connect class to implement a wrapper for an **Inspectors** collection.</span></span> <span data-ttu-id="48afa-108">Второй пример кода показывает простую реализацию класса **OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="48afa-108">The second code example involves a simple implementation of the **OutlookInspector** class.</span></span>

<span data-ttu-id="48afa-109">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="48afa-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="48afa-110">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="48afa-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="48afa-111">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="48afa-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="48afa-112">В представленном ниже примере кода [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) событие возникает после создания нового окна инспектора и перед его отображением.</span><span class="sxs-lookup"><span data-stu-id="48afa-112">In the following code example, a [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) event occurs after a new inspector window has been created and before it is displayed.</span></span> <span data-ttu-id="48afa-113">Действием пользователя также можно создать новое окно инспектора.</span><span class="sxs-lookup"><span data-stu-id="48afa-113">A user action may also create a new inspector window.</span></span> <span data-ttu-id="48afa-114">В классе **Connect** объявлена переменная экземпляра уровня класса с именем inspectors, и обрабатывается событие **NewInspector**.</span><span class="sxs-lookup"><span data-stu-id="48afa-114">A class-level instance variable named inspectors in the **Connect** class is declared, and a **NewInspector** event is hooked up.</span></span> 

<span data-ttu-id="48afa-115">В методе inspectors\_NewInspector метод **FindOutlookInspector** проверяет, находится ли уже новое окно инспектора в списке inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="48afa-115">In the inspectors\_NewInspector method, the **FindOutlookInspector** method checks whether the new inspector window is already in the inspectorWindows list.</span></span> <span data-ttu-id="48afa-116">Если FindOutlookInspector не может найти объект **Inspector** в inspectorWindows, метод **AddInspector** добавляет экземпляр класса **OutlookInspector** в список inspectorWindows.</span><span class="sxs-lookup"><span data-stu-id="48afa-116">If FindOutlookInspector does not find the **Inspector** object in inspectorWindows, the **AddInspector** method adds an instance of the **OutlookInspector** class to inspectorWindows.</span></span> <span data-ttu-id="48afa-117">Класс **OutlookInspector** можно использовать, чтобы создать события для этого конкретного окна инспектора.</span><span class="sxs-lookup"><span data-stu-id="48afa-117">You can use the **OutlookInspector** class to raise events for this particular inspector window.</span></span> <span data-ttu-id="48afa-118">Реализация класса **OutlookInspector** показана во втором примере кода.</span><span class="sxs-lookup"><span data-stu-id="48afa-118">The implementation of the **OutlookInspector** class is shown in the second code example.</span></span>

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

<span data-ttu-id="48afa-119">Следующий пример кода является реализацией класса **OutlookInspector**.</span><span class="sxs-lookup"><span data-stu-id="48afa-119">The following code example is an implementation of the **OutlookInspector** class.</span></span> <span data-ttu-id="48afa-120">Этот класс используется, чтобы создавать события для окна инспектора из предыдущего примера кода.</span><span class="sxs-lookup"><span data-stu-id="48afa-120">This class is used to raise events for the inspector window from the preceding code example.</span></span> <span data-ttu-id="48afa-121">Одновременно можно открыть несколько окон инспекторов.</span><span class="sxs-lookup"><span data-stu-id="48afa-121">Multiple inspector windows can be open simultaneously.</span></span> <span data-ttu-id="48afa-122">События уровня элемента, такие как [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) и [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)), отслеживаются с помощью обработчиков, задаваемых в конструкторе этого класса.</span><span class="sxs-lookup"><span data-stu-id="48afa-122">Item-level events such as [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)), and [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) are tracked by hooking them up in this class constructor.</span></span> <span data-ttu-id="48afa-123">Событие [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) для объекта [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) также обрабатывается в конструкторе этого класса.</span><span class="sxs-lookup"><span data-stu-id="48afa-123">A [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) event for a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is also hooked up in this class constructor.</span></span> <span data-ttu-id="48afa-124">При необходимости можно задать другие переменные экземпляра элемента уровня класса.</span><span class="sxs-lookup"><span data-stu-id="48afa-124">You can define other class-level item instance variables as needed.</span></span> <span data-ttu-id="48afa-125">Все события, обработчики которых подключены в конструкторе OutlookInspector, освобождаются в обработчике события OutlookInspectorWindow\_Close.</span><span class="sxs-lookup"><span data-stu-id="48afa-125">All the events that were hooked up in the OutlookInspector constructor are unhooked in the OutlookInspectorWindow\_Close event handler.</span></span>

<span data-ttu-id="48afa-126">Обратите внимание, что на уровне объектной модели объект **Outlook inspector** не относится к какому-либо элементу Outlook.</span><span class="sxs-lookup"><span data-stu-id="48afa-126">Note that at the object model level, an **Outlook inspector** object is not specific to any Outlook item type.</span></span> <span data-ttu-id="48afa-127">В этом примере кода используется вспомогательный класс OutlookItem, определенный в статье [Создание вспомогательного класса для доступа к распространенным элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), чтобы легко вызывать свойство OutlookItem.Class для проверки класса сообщений текущего элемента в инспекторе до предположения, что элемент является элементом контактов.</span><span class="sxs-lookup"><span data-stu-id="48afa-127">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of the current item in the inspector, before assuming the item is a contact item.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="48afa-128">См. также</span><span class="sxs-lookup"><span data-stu-id="48afa-128">See also</span></span>

- [<span data-ttu-id="48afa-129">Примеры задач, в которых используются события Outlook</span><span class="sxs-lookup"><span data-stu-id="48afa-129">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

