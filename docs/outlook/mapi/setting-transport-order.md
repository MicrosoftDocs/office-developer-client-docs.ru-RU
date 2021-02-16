---
title: Настройка порядка транспорта
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
# <a name="setting-transport-order"></a><span data-ttu-id="d2f4a-103">Настройка порядка транспорта</span><span class="sxs-lookup"><span data-stu-id="d2f4a-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="d2f4a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2f4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2f4a-105">Пулер MAPI назначает ответственность за исходяние сообщений на основе типов адресов и идентификаторов, которые поставщики транспорта объявляют, что они могут обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="d2f4a-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="d2f4a-106">Поставщики транспорта публикуют список поддерживаемых типов адресов и идентификаторов, хранимых в структурах **MAPIUID,** когда MAPI вызывает их метод [IXPLogon::AddressTypes](ixplogon-addresstypes.md) непосредственно после логарифма.</span><span class="sxs-lookup"><span data-stu-id="d2f4a-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="d2f4a-107">Тип адреса получателя хранится в его свойстве **PR_ADDRTYPE** ([PidTagAddressType).](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d2f4a-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d2f4a-108">Регистрация для типа адреса указывает MAPI, что поставщик транспорта может  доставить получателям с PR_ADDRTYPE свойства зарегистрированного типа адреса.</span><span class="sxs-lookup"><span data-stu-id="d2f4a-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="d2f4a-109">Аналогичным образом, регистрация **MAPIUID** означает, что поставщик транспорта может доставить получателям, представленным идентификаторами записей с зарегистрированным **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="d2f4a-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="d2f4a-110">Большинство поставщиков транспорта регистрируются для одного или более типов адресов; несколько регистрируются **с помощью MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="d2f4a-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="d2f4a-111">Поставщики транспорта, тесно совмещение с поставщиком адресной книги и понимание формата идентификатора записи, могут регистрироваться для обработки сообщений с помощью **MAPIUID,** тем самым повышая производительность.</span><span class="sxs-lookup"><span data-stu-id="d2f4a-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="d2f4a-112">Эти тесно сжатые поставщики транспорта могут извлечь адрес электронной почты получателя и другие необходимые сведения из идентификатора записи, не открывая его с помощью вызова **IMAPISupport::OpenEntry.**</span><span class="sxs-lookup"><span data-stu-id="d2f4a-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="d2f4a-113">MAPI поддерживает порядок для поставщиков транспорта, используемый при регистрации нескольких поставщиков транспорта для одного типа адреса или **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="d2f4a-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="d2f4a-114">Этот порядок можно переопредить, вызывая [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) и передавая упорядоченный список **mapIUID** всех активных поставщиков транспорта, на которые указывает параметр _lpUIDList.:_</span><span class="sxs-lookup"><span data-stu-id="d2f4a-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID** s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="d2f4a-115">Чтобы получить список всех типов адресов, которые могут обрабатываться одним из активных поставщиков транспорта, вызовите [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="d2f4a-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="d2f4a-116">**EnumAdrTypes** возвращает массив строк, описывая типы адресов, поддерживаемые поставщиками транспорта, которые активны в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="d2f4a-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

