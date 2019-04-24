---
title: Настройка трансПортного заказа
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339391"
---
# <a name="setting-transport-order"></a><span data-ttu-id="892a9-103">Настройка трансПортного заказа</span><span class="sxs-lookup"><span data-stu-id="892a9-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="892a9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="892a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="892a9-105">Диспетчер очереди MAPI назначает ответственность за исходящие сообщения на основе типов и идентификаторов, которые могут быть обработаны поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="892a9-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="892a9-106">Поставщики транспорта публикуют список поддерживаемых типов адресов и идентификаторов, хранимых в структурах **мапиуид** , когда MAPI вызывает метод [Иксплогон:: аддресстипес](ixplogon-addresstypes.md) непосредственно после входа.</span><span class="sxs-lookup"><span data-stu-id="892a9-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="892a9-107">Тип адреса получателя хранится в свойстве **пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="892a9-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="892a9-108">Регистрация для типа адреса указывает на MAPI, что поставщик транспорта может доставить получателям, у которых свойство **пр_аддртипе** имеет значение зарегистрированный тип адреса.</span><span class="sxs-lookup"><span data-stu-id="892a9-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="892a9-109">Аналогично, регистрация для **мапиуид** указывает, что поставщик транспорта может доставить получателям, представленным идентификаторами записей, зарегистрированным **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="892a9-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="892a9-110">Большинство поставщиков транспорта регистрируются для одного или нескольких типов адресов; малое количество регистров в **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="892a9-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="892a9-111">Поставщики транспорта, тесно связанные с поставщиком адресных книг и изменяющие свой формат идентификатора записи, могут регистрироваться для обработки сообщений с помощью **мапиуид**, что повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="892a9-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="892a9-112">Эти тесно связанные транспортные поставщики могут извлекать адрес электронной почты получателя и другие необходимые сведения из идентификатора записи, не открывая их с помощью вызова **имаписуппорт:: OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="892a9-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="892a9-113">MAPI поддерживает порядок для поставщиков транспорта, который используется, когда несколько поставщиков транспорта зарегистрированы для одного и того же типа адресов или **мапиуид**.</span><span class="sxs-lookup"><span data-stu-id="892a9-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="892a9-114">Вы можете переопределить этот порядок, вызвав [имсгсервицеадмин:: мсгсервицетранспортордер](imsgserviceadmin-msgservicetransportorder.md) и передав упорядоченный список **мапиуид**s всех активных поставщиков транспорта, на который указывает параметр _лпуидлист_ .:</span><span class="sxs-lookup"><span data-stu-id="892a9-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="892a9-115">Чтобы получить список всех типов адресов, которые могут обрабатываться одним из активных поставщиков транспорта, вызовите метод [IMAPISession:: енумадртипес](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="892a9-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="892a9-116">**Енумадртипес** возвращает массив строк, описывающих типы адресов, поддерживаемые поставщиками транспорта, которые активны в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="892a9-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

