---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Представляет структуру ACCT_BIN, которая содержит UID учетной записи Exchange учетной записи.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326553"
---
# <a name="prop_mapi_emsmdb_uid"></a><span data-ttu-id="1e751-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="1e751-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="1e751-104">Представляет [структуру ACCT_BIN,](acct_bin.md) которая содержит UID учетной записи Exchange учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1e751-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="1e751-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1e751-105">Quick info</span></span>

<span data-ttu-id="1e751-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="1e751-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e751-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1e751-107">Identifier:</span></span>  <br/> |<span data-ttu-id="1e751-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="1e751-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="1e751-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="1e751-109">Property type:</span></span>  <br/> |<span data-ttu-id="1e751-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1e751-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1e751-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="1e751-111">Property tag:</span></span>  <br/> |<span data-ttu-id="1e751-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="1e751-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="1e751-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="1e751-113">Access:</span></span>  <br/> |<span data-ttu-id="1e751-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e751-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e751-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e751-115">Remarks</span></span>

<span data-ttu-id="1e751-116">Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="1e751-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="1e751-117">Используйте [PROP_ACCT_IS_EXCH,](prop_acct_is_exch.md) чтобы проверить, является ли учетная запись Exchange учетной записью.</span><span class="sxs-lookup"><span data-stu-id="1e751-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="1e751-118">Если это так, **prop \_ MAPI_EMSMDB_UID**  является ACCT_BIN, который содержит **emsmdbUID**, который является уникальным ID, для Exchange учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1e751-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="1e751-119">Если учетная запись не является Exchange учетной записью, это свойство не является неопределенным.</span><span class="sxs-lookup"><span data-stu-id="1e751-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e751-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1e751-120">See also</span></span>

- [<span data-ttu-id="1e751-121">Сведения об API управления учетными записями</span><span class="sxs-lookup"><span data-stu-id="1e751-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="1e751-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="1e751-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="1e751-123">Использование нескольких Exchange учетных записей</span><span class="sxs-lookup"><span data-stu-id="1e751-123">Using Multiple Exchange Accounts</span></span>](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="1e751-124">������������ �������� PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="1e751-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

