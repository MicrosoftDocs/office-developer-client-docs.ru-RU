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
ms.openlocfilehash: 80e933f5723746dbaeb39271cc813eb0ea56a705
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571187"
---
# <a name="mapi-address-types"></a><span data-ttu-id="90a26-103">Типы адресов MAPI</span><span class="sxs-lookup"><span data-stu-id="90a26-103">MAPI Address Types</span></span>

  
  
<span data-ttu-id="90a26-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90a26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90a26-105">Каждый пользователь с сообщениями связан с тип адреса символ строка, описывающая формат адрес пользователя, которая хранится в свойстве **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="90a26-105">Every messaging user is associated with an address type, a character string describing the format of the user's address that is stored in the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span> <span data-ttu-id="90a26-106">Сопоставление типов адресов форматов адресов.</span><span class="sxs-lookup"><span data-stu-id="90a26-106">Address types map to address formats.</span></span> <span data-ttu-id="90a26-107">То есть просмотрев тип адреса получателя, клиентские приложения можно определить форматирование адреса для получателя.</span><span class="sxs-lookup"><span data-stu-id="90a26-107">That is, by looking at a recipient's address type, client applications can determine how to format an address appropriate for the recipient.</span></span> 
  
<span data-ttu-id="90a26-108">Например `SMTP` указывает тип адреса стандартных веб-адрес:</span><span class="sxs-lookup"><span data-stu-id="90a26-108">For example, the  `SMTP` address type specifies the standard Internet address:</span></span> 
  
 `username@companyname.com.`
  
<span data-ttu-id="90a26-109">И `EX` тип адреса указывает адрес сервера Exchange.</span><span class="sxs-lookup"><span data-stu-id="90a26-109">And, the  `EX` address type specifies an Exchange Server address.</span></span> 
  
<span data-ttu-id="90a26-110">Все записи адресной книги должен иметь допустимый адрес тип.</span><span class="sxs-lookup"><span data-stu-id="90a26-110">All address book entries must have a valid address type.</span></span> <span data-ttu-id="90a26-111">Клиентам требуется своим пользователям указать тип адреса при создании типа настраиваемого получателя не поддерживается поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="90a26-111">Clients require their users to specify an address type when creating a type of custom recipient unsupported by the address book provider.</span></span> <span data-ttu-id="90a26-112">Для записи, которые они поддерживают поставщиками адресной книги необходимо предоставить допустимый адрес типы.</span><span class="sxs-lookup"><span data-stu-id="90a26-112">For the entries that they support, address book providers are required to supply valid address types.</span></span> 
  
<span data-ttu-id="90a26-113">MAPI определяет тип только один адрес: MAPIPDL, соответствующий списку рассылки.</span><span class="sxs-lookup"><span data-stu-id="90a26-113">MAPI defines only one address type: MAPIPDL, which stands for personal distribution list.</span></span>
  
<span data-ttu-id="90a26-114">Чтобы получить список типов адресов, поддерживаемые всеми поставщиками транспорта в сеансе, клиентские приложения вызовите метод **IMAPISession::EnumAdrTypes** .</span><span class="sxs-lookup"><span data-stu-id="90a26-114">To get a list of the address types supported by all of the transport providers in the session, client applications call the **IMAPISession::EnumAdrTypes** method.</span></span> <span data-ttu-id="90a26-115">Для получения дополнительных сведений см [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="90a26-115">For more information, see [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span>
  

