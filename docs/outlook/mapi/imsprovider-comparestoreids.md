---
title: имспровидеркомпарестореидс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431710"
---
# <a name="imsprovidercomparestoreids"></a><span data-ttu-id="82f7e-103">IMSProvider::CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="82f7e-103">IMSProvider::CompareStoreIDs</span></span>

  
  
<span data-ttu-id="82f7e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82f7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82f7e-105">Сравнивает два идентификатора записи хранилища сообщений, чтобы определить, ссылаются ли они на один и тот же объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="82f7e-105">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>
  
```cpp
HRESULT CompareStoreIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a><span data-ttu-id="82f7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82f7e-106">Parameters</span></span>

 <span data-ttu-id="82f7e-107">_cbEntryID1_</span><span class="sxs-lookup"><span data-stu-id="82f7e-107">_cbEntryID1_</span></span>
  
> <span data-ttu-id="82f7e-108">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID1_ _._</span><span class="sxs-lookup"><span data-stu-id="82f7e-108">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID1_ parameter  _._</span></span>
    
 <span data-ttu-id="82f7e-109">_lpEntryID1_</span><span class="sxs-lookup"><span data-stu-id="82f7e-109">_lpEntryID1_</span></span>
  
> <span data-ttu-id="82f7e-110">возврата Указатель на первый идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="82f7e-110">[in] A pointer to the first entry identifier to be compared.</span></span>
    
 <span data-ttu-id="82f7e-111">_cbEntryID2_</span><span class="sxs-lookup"><span data-stu-id="82f7e-111">_cbEntryID2_</span></span>
  
> <span data-ttu-id="82f7e-112">возврата Размер (в байтах) идентификатора записи, на который указывает параметр _lpEntryID2_ _._</span><span class="sxs-lookup"><span data-stu-id="82f7e-112">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID2_ parameter  _._</span></span>
    
 <span data-ttu-id="82f7e-113">_lpEntryID2_</span><span class="sxs-lookup"><span data-stu-id="82f7e-113">_lpEntryID2_</span></span>
  
> <span data-ttu-id="82f7e-114">возврата Указатель на второй идентификатор записи, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="82f7e-114">[in] A pointer to the second entry identifier to be compared.</span></span>
    
 <span data-ttu-id="82f7e-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82f7e-115">_ulFlags_</span></span>
  
> <span data-ttu-id="82f7e-116">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="82f7e-116">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="82f7e-117">_лпулресулт_</span><span class="sxs-lookup"><span data-stu-id="82f7e-117">_lpulResult_</span></span>
  
> <span data-ttu-id="82f7e-118">вышли Указатель на возвращаемый результат сравнения.</span><span class="sxs-lookup"><span data-stu-id="82f7e-118">[out] A pointer to the returned result of the comparison.</span></span> <span data-ttu-id="82f7e-119">Значение TRUE, если два идентификатора записи ссылаются на один объект; в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="82f7e-119">TRUE if the two entry identifiers refer to the same object; otherwise, FALSE.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82f7e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82f7e-120">Return value</span></span>

<span data-ttu-id="82f7e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="82f7e-121">S_OK</span></span> 
  
> <span data-ttu-id="82f7e-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="82f7e-122">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82f7e-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="82f7e-123">Remarks</span></span>

<span data-ttu-id="82f7e-124">MAPI вызывает метод **функцииimsprovider:: компарестореидс** при обработке вызова метода [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="82f7e-124">MAPI calls the **IMSProvider::CompareStoreIDs** method when it processes a call to the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="82f7e-125">В этой точке вызывается **компарестореидс** , чтобы определить, какой раздел профиля связан с открываемым хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="82f7e-125">**CompareStoreIDs** is called at this point to determine which profile section, if any, is associated with the message store being opened.</span></span> <span data-ttu-id="82f7e-126">Вызов **компарестореидс** можно выполнить, если нет открытых хранилищ сообщений для конкретного поставщика услуг хранения.</span><span class="sxs-lookup"><span data-stu-id="82f7e-126">A **CompareStoreIDs** call can be made when no message stores are open for a particular store provider.</span></span> <span data-ttu-id="82f7e-127">Кроме того, MAPI также вызывает **компарестореидс** , когда он обрабатывает вызов поставщика хранилища в метод [Имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="82f7e-127">In addition, MAPI also calls **CompareStoreIDs** when it processes a store provider call to the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method.</span></span> 
  
<span data-ttu-id="82f7e-128">Идентификаторы записей, по сравнению с **компарестореидс** , предназначены для библиотеки динамической компоновки (DLL) текущего поставщика хранилища (DLL) и являются неупакованными идентификаторами записей в хранилище.</span><span class="sxs-lookup"><span data-stu-id="82f7e-128">The entry identifiers compared by **CompareStoreIDs** are both for the current store provider's dynamic-link library (DLL) and are both unwrapped store entry identifiers.</span></span> <span data-ttu-id="82f7e-129">Дополнительные сведения о переносе идентификаторов записей в хранилище можно найти в статье [имаписуппорт:: врапсторинтрид](imapisupport-wrapstoreentryid.md).</span><span class="sxs-lookup"><span data-stu-id="82f7e-129">For more information about wrapping store entry identifiers, see [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md).</span></span>
  
<span data-ttu-id="82f7e-130">Возможность сравнения идентификаторов записей полезна, так как объект может иметь несколько допустимых идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="82f7e-130">Comparing entry identifiers is useful because an object can have more than one valid entry identifier.</span></span> <span data-ttu-id="82f7e-131">Это может произойти, например, после установки новой версии поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="82f7e-131">This can occur, for example, after a new version of a message store provider is installed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82f7e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="82f7e-132">See also</span></span>



[<span data-ttu-id="82f7e-133">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="82f7e-133">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="82f7e-134">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="82f7e-134">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="82f7e-135">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="82f7e-135">IMAPISupport::WrapStoreEntryID</span></span>](imapisupport-wrapstoreentryid.md)
  
[<span data-ttu-id="82f7e-136">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82f7e-136">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

