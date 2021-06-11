---
title: Настройка порядка транспортировки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433600"
---
# <a name="setting-transport-order"></a><span data-ttu-id="b2737-103">Настройка порядка транспортировки</span><span class="sxs-lookup"><span data-stu-id="b2737-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="b2737-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2737-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2737-105">Spooler MAPI назначает ответственность за исходяние сообщений на основе типов адресов и идентификаторов, которые поставщики транспорта заявляют, что они могут обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="b2737-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="b2737-106">Поставщики транспорта публикуют список поддерживаемых типов адресов и идентификаторов, хранимых в структурах **MAPIUID,** когда MAPI вызывает их [метод IXPLogon::AddressTypes](ixplogon-addresstypes.md) непосредственно после логотипа.</span><span class="sxs-lookup"><span data-stu-id="b2737-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="b2737-107">Тип адреса получателя хранится в **свойстве PR_ADDRTYPE** [(PidTagAddressType).](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b2737-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="b2737-108">Регистрация типа адресов указывает MAPI, что поставщик транспорта может доставить  получателям PR_ADDRTYPE свойства, заданная для зарегистрированного типа адреса.</span><span class="sxs-lookup"><span data-stu-id="b2737-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="b2737-109">Кроме того, регистрация **mapIUID** указывает, что поставщик транспорта может доставить получателям, представленным идентификаторами входа с зарегистрированным **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="b2737-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="b2737-110">Большинство поставщиков транспорта регистрируются для одного или более типов адресов; немногие зарегистрироваться **в MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="b2737-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="b2737-111">Поставщики транспорта, тесно соединая с поставщиком адресной книги и понимаюющие формат идентификатора записи, могут регистрироваться для обработки сообщений **mapIUID,** тем самым повышая производительность.</span><span class="sxs-lookup"><span data-stu-id="b2737-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="b2737-112">Эти поставщики транспорта с тесной связи могут извлекать адрес электронной почты получателя и другие необходимые сведения из идентификатора записи, не открывая его с помощью **вызова IMAPISupport::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="b2737-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="b2737-113">MAPI поддерживает порядок для поставщиков транспорта, используемый при регистрации нескольких поставщиков транспорта для одного типа адресов или **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="b2737-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="b2737-114">Переопределять этот порядок можно, позвонив [в IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) и передав упорядоченный список **mapIUID** s всех активных поставщиков транспорта, на которые указывает параметр _lpUIDList.:_</span><span class="sxs-lookup"><span data-stu-id="b2737-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID** s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="b2737-115">Чтобы получить список всех типов адресов, которые могут обрабатываться одним из активных поставщиков транспорта, позвоните [в службу IMAPISession::EnumAdrTypes.](imapisession-enumadrtypes.md)</span><span class="sxs-lookup"><span data-stu-id="b2737-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="b2737-116">**EnumAdrTypes** возвращает массив строк, которые описывают типы адресов, поддерживаемые поставщиками транспорта, активными в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="b2737-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

