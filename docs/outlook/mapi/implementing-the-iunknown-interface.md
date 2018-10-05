---
title: Реализация интерфейса IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397417"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="00691-103">Реализация интерфейса IUnknown</span><span class="sxs-lookup"><span data-stu-id="00691-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="00691-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00691-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00691-105">Методы интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , реализованный в каждый объект MAPI поддерживают способ управления обмена данными и объекта.</span><span class="sxs-lookup"><span data-stu-id="00691-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="00691-106">**Интерфейс IUnknown** имеет три метода: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)и [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="00691-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="00691-107">**QueryInterface** включает один объект, который требуется определить, поддерживает ли другой объект определенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="00691-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="00691-108">**QueryInterface**могут работать два объекта с отсутствуют знания функциональные возможности друг друга.</span><span class="sxs-lookup"><span data-stu-id="00691-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="00691-109">Если объект, который реализует **QueryInterface** поддерживают интерфейс интересующую, возвращает указатель на реализацию интерфейса.</span><span class="sxs-lookup"><span data-stu-id="00691-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="00691-110">Если объект не поддерживает запрошенный интерфейс, возвращается значение MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="00691-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="00691-111">При **QueryInterface** возвращает указатель на интерфейс, его необходимо также увеличить счетчик ссылок новый объект.</span><span class="sxs-lookup"><span data-stu-id="00691-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="00691-112">Счетчик ссылку на объект — числовое значение, используемый для управления объекта зависящая от.</span><span class="sxs-lookup"><span data-stu-id="00691-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="00691-113">Если счетчик ссылок больше 1, так как он активно используется не может освободить память объекта.</span><span class="sxs-lookup"><span data-stu-id="00691-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="00691-114">Это, только когда счетчик ссылок станет равен 0, что объект безопасно можно отменить.</span><span class="sxs-lookup"><span data-stu-id="00691-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="00691-115">Другие два методы **IUnknown** , **AddRef** и **выпуска**, управление счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="00691-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="00691-116">**Метод AddRef** увеличивает счетчик ссылок, при **выпуске** уменьшает его.</span><span class="sxs-lookup"><span data-stu-id="00691-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="00691-117">Все методы или функции API, которые возвращают указатели интерфейса, таких как **QueryInterface**, необходимо вызвать **метод AddRef** для увеличивают счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="00691-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="00691-118">Все реализации методов, которые получают указателей интерфейса необходимо вызвать **выпуска** для уменьшения count, когда указатель мыши больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="00691-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="00691-119">**Выпуск** проверяет наличие существующего счетчик ссылок, освободить память, связанные с интерфейсом только в том случае, если число равняется 0.</span><span class="sxs-lookup"><span data-stu-id="00691-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00691-120">Так как **AddRef** и **Release** не требуются для возвращения точных значений, звонящих из этих методов нельзя использовать возвращаемые значения для определения ли объект еще не истек или был удален.</span><span class="sxs-lookup"><span data-stu-id="00691-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00691-121">См. также</span><span class="sxs-lookup"><span data-stu-id="00691-121">See also</span></span>



[<span data-ttu-id="00691-122">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="00691-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

