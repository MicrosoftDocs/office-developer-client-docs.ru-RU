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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315521"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="7a32d-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="7a32d-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="7a32d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a32d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a32d-105">Предоставляет объект хранилища протокола IMAP, который был развернут и предоставляет доступ к элементам в файле личных папок (PST), не вызывая синхронизацию и не загружая элементы.</span><span class="sxs-lookup"><span data-stu-id="7a32d-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7a32d-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7a32d-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a32d-107">Наследуется от:</span><span class="sxs-lookup"><span data-stu-id="7a32d-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="7a32d-108">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="7a32d-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="7a32d-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="7a32d-109">Provided By:</span></span>  <br/> |<span data-ttu-id="7a32d-110">Поставщик хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="7a32d-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="7a32d-111">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="7a32d-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7a32d-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="7a32d-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7a32d-113">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="7a32d-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="7a32d-114">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="7a32d-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="7a32d-115">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="7a32d-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="7a32d-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="7a32d-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="7a32d-117">Получает указатель на неупакованное хранилище IMAP.</span><span class="sxs-lookup"><span data-stu-id="7a32d-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="7a32d-118">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="7a32d-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="7a32d-119">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="7a32d-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a32d-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a32d-120">Remarks</span></span>

<span data-ttu-id="7a32d-121">Вызовите метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) в исходном хранилище сообщений для получения интерфейса **ипроксистореобжект** .</span><span class="sxs-lookup"><span data-stu-id="7a32d-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="7a32d-122">Затем вызовите **ипроксистореобжект:: унврапнореф** , чтобы получить объект неупакованного хранилища.</span><span class="sxs-lookup"><span data-stu-id="7a32d-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="7a32d-123">Если **QueryInterface** возвращает ошибку **MAPI_E_INTERFACE_NOT_SUPPORTED**, то хранилище не было заключено в оболочку.</span><span class="sxs-lookup"><span data-stu-id="7a32d-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="7a32d-124">Так как **унврапнореф** не увеличивает значение счетчика ссылок для нового указателя на неупакованный объект Store после успешного вызова **унврапнореф**, необходимо вызвать метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержания счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="7a32d-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

