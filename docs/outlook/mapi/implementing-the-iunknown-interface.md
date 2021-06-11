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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310047"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="897ec-103">Реализация интерфейса IUnknown</span><span class="sxs-lookup"><span data-stu-id="897ec-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="897ec-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="897ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="897ec-105">Методы интерфейса [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) реализованные в каждом объекте MAPI, поддерживают межобъективную связь и управление объектами.</span><span class="sxs-lookup"><span data-stu-id="897ec-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="897ec-106">**IUnknown** имеет три метода: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)и [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="897ec-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="897ec-107">**QueryInterface** позволяет одному объекту определить, поддерживает ли другой объект определенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="897ec-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="897ec-108">С **Помощью QueryInterface** могут взаимодействовать два объекта без предварительного знания функциональности друг друга.</span><span class="sxs-lookup"><span data-stu-id="897ec-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="897ec-109">Если объект, реализующий **QueryInterface,** поддерживает данный интерфейс, он возвращает указатель на реализацию интерфейса.</span><span class="sxs-lookup"><span data-stu-id="897ec-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="897ec-110">Если объект не поддерживает запрашиваемой интерфейс, он возвращает MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="897ec-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="897ec-111">Когда **RequestInterface** возвращает запрашиваемую указатель интерфейса, он также должен увеличить число ссылок нового объекта.</span><span class="sxs-lookup"><span data-stu-id="897ec-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="897ec-112">Число ссылок объекта — это числовая величина, используемая для управления продолжительности жизни объекта.</span><span class="sxs-lookup"><span data-stu-id="897ec-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="897ec-113">Если количество ссылок превышает 1, память объекта не может быть освобождена, так как она активно используется.</span><span class="sxs-lookup"><span data-stu-id="897ec-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="897ec-114">Только когда количество ссылок падает до 0, объект можно безопасно освободить.</span><span class="sxs-lookup"><span data-stu-id="897ec-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="897ec-115">Два других **метода IUnknown,** **AddRef** и **Release,** управляют количеством ссылок.</span><span class="sxs-lookup"><span data-stu-id="897ec-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="897ec-116">**AddRef** добавляет количество ссылок, в то время как **Release** его приумношает.</span><span class="sxs-lookup"><span data-stu-id="897ec-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="897ec-117">Все методы или функции API, возвращающих указатели интерфейса, такие как **QueryInterface,** должны вызывать **AddRef,** чтобы прибавить количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="897ec-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="897ec-118">Все реализации методов, которые получают указатели интерфейса, должны вызывать **Release,** чтобы отпустить количество, когда указатель больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="897ec-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="897ec-119">**Отпустите** проверки существующего эталонного счета, освободив память, связанную с интерфейсом, только если количество 0.</span><span class="sxs-lookup"><span data-stu-id="897ec-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="897ec-120">Поскольку **addRef** и **Release** не требуются для возврата точных значений, вызыватели этих методов не должны использовать значения возврата, чтобы определить, является ли объект по-прежнему допустимым или был уничтожен.</span><span class="sxs-lookup"><span data-stu-id="897ec-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="897ec-121">См. также</span><span class="sxs-lookup"><span data-stu-id="897ec-121">See also</span></span>



[<span data-ttu-id="897ec-122">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="897ec-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

