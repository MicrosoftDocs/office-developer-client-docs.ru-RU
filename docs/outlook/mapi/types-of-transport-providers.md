---
title: Типы поставщиков транспорта
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406166"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="b1d4e-103">Типы поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="b1d4e-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="b1d4e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1d4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1d4e-105">Все поставщики транспорта поддерживают ряд стандартных функций, таких как:</span><span class="sxs-lookup"><span data-stu-id="b1d4e-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="b1d4e-106">Обеспечение надлежащей безопасности для базовой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="b1d4e-107">Отправка и получение сообщений из базовой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="b1d4e-108">Предоставление типов адресов, поддерживаемых поставщиками транспорта, поэтому диспетчер очереди MAPI и клиентские приложения могут использовать их соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="b1d4e-109">Принятие доставки для определенных получателей.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="b1d4e-110">Кроме того, MAPI поддерживает два специализированных типа поставщиков для определенных систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="b1d4e-111">**Тип транспорта**</span><span class="sxs-lookup"><span data-stu-id="b1d4e-111">**Transport type**</span></span>|<span data-ttu-id="b1d4e-112">**Добавлена функциональная возможность**</span><span class="sxs-lookup"><span data-stu-id="b1d4e-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1d4e-113">Удаленный транспорт</span><span class="sxs-lookup"><span data-stu-id="b1d4e-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="b1d4e-114">Обеспечивает взаимодействие с клиентами, подключенными удаленно.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="b1d4e-115">Транспорт TNEF</span><span class="sxs-lookup"><span data-stu-id="b1d4e-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="b1d4e-116">Позволяет сохранять свойства MAPI в системах обмена сообщениями, не поддерживающих их.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="b1d4e-117">Транспорты TNEF используются для преобразования сообщений между системами обмена сообщениями, которые поддерживают различные наборы свойств MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="b1d4e-118">Для транспорта TNEF используется интерфейс [IUnknown итнеф: интерфейс IUnknown](itnefiunknown.md) , чтобы преобразовать все свойства, которые конечная система не может представить непосредственно в поток двоичных данных, который можно вложить в сообщение.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="b1d4e-119">Позже еще один транспорт TNEF может использовать **итнеф** для декодирования потока данных и предоставления доступа к исходным свойствам MAPI для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="b1d4e-120">Кроме того, в случае необходимости поддержки пользовательских классов сообщений в транспорте требуется поддержка формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="b1d4e-121">Сведения о реализации транспорта TNEF приведены [в статье Разработка поставщика транспорта с поддержкой TNEF](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b1d4e-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="b1d4e-122">Если ваш поставщик транспорта не является одним из этих типов, необходимо реализовать его с помощью базовых функций MAPI и сетевых функций, доступных на целевой платформе.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

