---
title: Установка порядка транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6e4c318678fdce7976140ff8f480ae638fd3ca4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593027"
---
# <a name="setting-transport-order"></a><span data-ttu-id="20c79-103">Установка порядка транспорта</span><span class="sxs-lookup"><span data-stu-id="20c79-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="20c79-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20c79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20c79-105">Диспетчер очереди MAPI назначает ответственность за на основе типов адресов и идентификаторы, которые поставщиками транспорта declare, они могут обрабатывать исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="20c79-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="20c79-106">Поставщиками транспорта опубликовать список поддерживаемых адрес типов и идентификаторы, хранящиеся в **MAPIUID** структуры — при MAPI вызывает метод их [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , непосредственно после входа в систему.</span><span class="sxs-lookup"><span data-stu-id="20c79-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="20c79-107">Тип адреса получателя хранится в свойстве **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="20c79-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="20c79-108">Регистрация для тип адреса указывает MAPI поставщика транспорта можно доставить получателям с их свойства **PR_ADDRTYPE** для типа зарегистрированных адреса.</span><span class="sxs-lookup"><span data-stu-id="20c79-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="20c79-109">Аналогично регистрация для **MAPIUID** указывает, что поставщик транспорта могут обеспечить получателям, представленными идентификаторы записей с зарегистрированным **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="20c79-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="20c79-110">Большинство поставщиков транспорта регистрация для одного или нескольких типов адресов; Минимальное количество регистрации с **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="20c79-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="20c79-111">Поставщики транспорта, которые тесно связаны с поставщика адресных книг и понять его формат идентификатора записи можно зарегистрировать для обработки сообщений с **MAPIUID**, тем самым повышение производительности.</span><span class="sxs-lookup"><span data-stu-id="20c79-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="20c79-112">Эти поставщики тесно связанных транспорта можно извлечь адрес электронной почты получателя и другие необходимые сведения из идентификатор записи без необходимости открывать вызовом **IMAPISupport::OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="20c79-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="20c79-113">MAPI поддерживает приоритет для поставщиками транспорта, используемый при регистрации нескольких поставщиков транспорта для одного типа адреса или **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="20c79-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="20c79-114">В этом порядке можно переопределить путем вызова [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) и передачи упорядоченный список s **MAPIUID**всех поставщиков активный перенос указывает параметр _lpUIDList_ .:</span><span class="sxs-lookup"><span data-stu-id="20c79-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="20c79-115">Чтобы получить список всех типов адресов, которые могут быть обработаны с помощью одного из поставщиков активный перенос, вызовите [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="20c79-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="20c79-116">**EnumAdrTypes** возвращает массив строк, описывающий типы адресов, поддерживаемые поставщиками транспорта, которые включены в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="20c79-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

