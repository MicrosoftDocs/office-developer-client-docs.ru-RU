---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395310"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="693fa-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="693fa-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="693fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="693fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="693fa-105">Содержит объект хранилища протокола доступа сообщения Интернета (IMAP), которая была оболочку и без вызова синхронизации и загрузку элементов, которая позволяет получить доступ к элементов в файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="693fa-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="693fa-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="693fa-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="693fa-107">Наследуется от:</span><span class="sxs-lookup"><span data-stu-id="693fa-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="693fa-108">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="693fa-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="693fa-109">Автор:</span><span class="sxs-lookup"><span data-stu-id="693fa-109">Provided By:</span></span>  <br/> |<span data-ttu-id="693fa-110">Поставщик хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="693fa-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="693fa-111">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="693fa-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="693fa-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="693fa-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="693fa-113">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="693fa-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="693fa-114">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="693fa-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="693fa-115">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="693fa-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="693fa-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="693fa-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="693fa-117">Получает указатель на хранилище оболочку IMAP.</span><span class="sxs-lookup"><span data-stu-id="693fa-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="693fa-118">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="693fa-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="693fa-119">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="693fa-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="693fa-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="693fa-120">Remarks</span></span>

<span data-ttu-id="693fa-121">Вызов [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) хранилища сообщений источника для получения интерфейса **IProxyStoreObject** .</span><span class="sxs-lookup"><span data-stu-id="693fa-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="693fa-122">Затем вызовите **IProxyStoreObject::UnwrapNoRef** , чтобы получить объект развернуть хранилища.</span><span class="sxs-lookup"><span data-stu-id="693fa-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="693fa-123">Если **QueryInterface** возвращает ошибку **MAPI_E_INTERFACE_NOT_SUPPORTED**, затем хранилище не заключен.</span><span class="sxs-lookup"><span data-stu-id="693fa-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="693fa-124">Так как **UnwrapNoRef** не увеличивает счетчик ссылок для этого нового указателя на объект оболочку хранилище после успешного вызова **UnwrapNoRef**, должны вызывать [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержки счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="693fa-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

