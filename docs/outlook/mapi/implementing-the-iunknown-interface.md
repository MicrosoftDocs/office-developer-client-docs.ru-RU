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
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="f261e-103">Реализация интерфейса IUnknown</span><span class="sxs-lookup"><span data-stu-id="f261e-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="f261e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f261e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f261e-105">Методы интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , реализованные в каждом объекте MAPI, поддерживают взаимодействие между объектами и управление объектами.</span><span class="sxs-lookup"><span data-stu-id="f261e-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="f261e-106">У **IUnknown** есть три метода: [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)и [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f261e-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="f261e-107">**QueryInterface** позволяет одному объекту определить, поддерживает ли другой объект определенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f261e-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="f261e-108">При использовании **QueryInterface**два объекта, не имеющие сведений о функциях друг друга, могут взаимодействовать друг с другом.</span><span class="sxs-lookup"><span data-stu-id="f261e-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="f261e-109">Если объект, реализующий **QueryInterface** , поддерживает рассматриваемый интерфейс, он возвращает указатель на реализацию интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f261e-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="f261e-110">Если объект не поддерживает запрошенный интерфейс, он возвращает значение МАПИ_Е_ИНТЕРФАЦЕ_НОТ_СУППОРТЕД.</span><span class="sxs-lookup"><span data-stu-id="f261e-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="f261e-111">Когда **QueryInterface** возвращает запрошенный указатель интерфейса, он также должен увеличить число ссылок нового объекта.</span><span class="sxs-lookup"><span data-stu-id="f261e-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="f261e-112">Число ссылок на объект — это числовое значение, используемое для управления сроком действия объекта.</span><span class="sxs-lookup"><span data-stu-id="f261e-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="f261e-113">Если значение счетчика ссылок больше 1, память объекта не может быть освобождена, так как она используется в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="f261e-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="f261e-114">Он используется только в том случае, когда число ссылок сбрасывается до 0, что объект может безопасно освобождаться.</span><span class="sxs-lookup"><span data-stu-id="f261e-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="f261e-115">Два других метода **IUnknown** , **AddRef** и **Release**, управляют счетчиком ссылок.</span><span class="sxs-lookup"><span data-stu-id="f261e-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="f261e-116">**AddRef** увеличивает значение счетчика ссылок, а при **отпускании** уменьшает его.</span><span class="sxs-lookup"><span data-stu-id="f261e-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="f261e-117">Все методы или функции API, возвращающие указатели на интерфейс, такие как **QueryInterface**, должны вызывать **AddRef** для увеличения числа ссылок.</span><span class="sxs-lookup"><span data-stu-id="f261e-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="f261e-118">Все реализации методов, которые получают указатели интерфейса, должны вызывать метод **Release** , чтобы уменьшить число, когда указатель больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="f261e-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="f261e-119">**Выпуск** выполняет проверку наличия существующего счетчика ссылок, освобождая память, связанную с интерфейсом, только если число равно 0.</span><span class="sxs-lookup"><span data-stu-id="f261e-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f261e-120">Так как **AddRef** и **Release** не являются обязательными для возврата точных значений, вызывающие методы этих методов не должны использовать возвращаемые значения для определения того, является ли объект допустимым или уничтоженным.</span><span class="sxs-lookup"><span data-stu-id="f261e-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f261e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f261e-121">See also</span></span>



[<span data-ttu-id="f261e-122">Реализация объектов MAPI</span><span class="sxs-lookup"><span data-stu-id="f261e-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

