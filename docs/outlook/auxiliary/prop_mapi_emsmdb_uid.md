---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Представляет структуру АККТ_БИН, которая содержит UID учетной записи Exchange.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326553"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="09ee9-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="09ee9-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="09ee9-104">Представляет структуру [аккт_бин](acct_bin.md) , которая содержит UID учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="09ee9-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="09ee9-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="09ee9-105">Quick info</span></span>

<span data-ttu-id="09ee9-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="09ee9-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09ee9-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="09ee9-107">Identifier:</span></span>  <br/> |<span data-ttu-id="09ee9-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="09ee9-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="09ee9-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="09ee9-109">Property type:</span></span>  <br/> |<span data-ttu-id="09ee9-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="09ee9-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="09ee9-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="09ee9-111">Property tag:</span></span>  <br/> |<span data-ttu-id="09ee9-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="09ee9-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="09ee9-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="09ee9-113">Access:</span></span>  <br/> |<span data-ttu-id="09ee9-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="09ee9-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09ee9-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="09ee9-115">Remarks</span></span>

<span data-ttu-id="09ee9-116">Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="09ee9-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="09ee9-117">Используйте [проп_аккт_ис_ексч](prop_acct_is_exch.md) , чтобы проверить, является ли учетная запись учетной записью Exchange.</span><span class="sxs-lookup"><span data-stu-id="09ee9-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="09ee9-118">Если это так, **prop\_Мапи_емсмдб_уид** — это **аккт_бин** , СОДЕРЖАЩИЙ **емсмдбуид**, который является уникальным идентификатором для учетной записи Exchange.</span><span class="sxs-lookup"><span data-stu-id="09ee9-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="09ee9-119">Если учетная запись не является учетной записью Exchange, это свойство не определено.</span><span class="sxs-lookup"><span data-stu-id="09ee9-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09ee9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="09ee9-120">See also</span></span>

- [<span data-ttu-id="09ee9-121">About the Account Management API</span><span class="sxs-lookup"><span data-stu-id="09ee9-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="09ee9-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="09ee9-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="09ee9-123">Использование нескольких учетных записей Exchange</span><span class="sxs-lookup"><span data-stu-id="09ee9-123">Using Multiple Exchange Accounts</span></span>](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="09ee9-124">������������ �������� PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="09ee9-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

