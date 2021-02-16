---
title: Типы адресов MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405438"
---
# <a name="mapi-address-types"></a><span data-ttu-id="fd43d-103">Типы адресов MAPI</span><span class="sxs-lookup"><span data-stu-id="fd43d-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="fd43d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd43d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd43d-105">Каждый пользователь сообщения связан с типом адреса, строкой символов, описывающий формат адреса пользователя, который хранится в свойстве **PR_ADDRTYPE** ([PidTagAddressType).](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="fd43d-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="fd43d-106">Типы адресов со картой форматов адресов.</span><span class="sxs-lookup"><span data-stu-id="fd43d-106">Address types map to address formats.</span></span> <span data-ttu-id="fd43d-107">То есть, изучая тип адреса получателя, клиентские приложения могут определить, как форматирование адреса, подходящего для получателя.</span><span class="sxs-lookup"><span data-stu-id="fd43d-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="fd43d-108">Например, тип  `SMTP` адреса указывает стандартный интернет-адрес:</span><span class="sxs-lookup"><span data-stu-id="fd43d-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="fd43d-109">А тип  `EX` адреса указывает Exchange Server адрес.</span><span class="sxs-lookup"><span data-stu-id="fd43d-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="fd43d-110">Все записи адресной книги должны иметь допустимый тип адреса.</span><span class="sxs-lookup"><span data-stu-id="fd43d-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="fd43d-111">Клиенты требуют, чтобы их пользователи указали тип адреса при создании типа настраиваемого получателя, неподтверченного поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="fd43d-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="fd43d-112">Для поддерживаемой записи поставщики адресных книг должны предоставить допустимые типы адресов.</span><span class="sxs-lookup"><span data-stu-id="fd43d-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="fd43d-113">MAPI определяет только один тип адреса: MAPIPDL, который обозначает личный список рассылки.</span><span class="sxs-lookup"><span data-stu-id="fd43d-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="fd43d-114">Чтобы получить список типов адресов, поддерживаемых всеми поставщиками транспорта в сеансе, клиентские приложения вызовят метод **IMAPISession::EnumAdrTypes.**</span><span class="sxs-lookup"><span data-stu-id="fd43d-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="fd43d-115">Дополнительные сведения см. в [подразделе IMAPISession::EnumAdrTypes.](imapisession-enumadrtypes.md)</span><span class="sxs-lookup"><span data-stu-id="fd43d-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

