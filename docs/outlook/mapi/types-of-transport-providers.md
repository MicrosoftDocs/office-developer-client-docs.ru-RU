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
# <a name="types-of-transport-providers"></a><span data-ttu-id="176ee-103">Типы поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="176ee-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="176ee-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="176ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="176ee-105">Все поставщики транспорта поддерживают ряд стандартных функций, таких как:</span><span class="sxs-lookup"><span data-stu-id="176ee-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="176ee-106">Обеспечение надлежащей безопасности для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="176ee-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="176ee-107">Отправка и получение сообщений из системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="176ee-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="176ee-108">Обнажая типы адресов, поддерживаемые поставщиками транспорта, чтобы пульпер MAPI и клиентские приложения могли использовать их надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="176ee-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="176ee-109">Прием доставки для определенных получателей.</span><span class="sxs-lookup"><span data-stu-id="176ee-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="176ee-110">Кроме того, MAPI поддерживает два специализированных типа поставщиков для определенных систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="176ee-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="176ee-111">**Тип транспорта**</span><span class="sxs-lookup"><span data-stu-id="176ee-111">**Transport type**</span></span>|<span data-ttu-id="176ee-112">**Добавлены функциональные возможности**</span><span class="sxs-lookup"><span data-stu-id="176ee-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="176ee-113">Удаленный транспорт</span><span class="sxs-lookup"><span data-stu-id="176ee-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="176ee-114">Обеспечивает связь с клиентами, подключенными удаленно.</span><span class="sxs-lookup"><span data-stu-id="176ee-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="176ee-115">Транспорт TNEF</span><span class="sxs-lookup"><span data-stu-id="176ee-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="176ee-116">Позволяет сохранять свойства MAPI в системах обмена сообщениями, которые их не поддерживают.</span><span class="sxs-lookup"><span data-stu-id="176ee-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="176ee-117">Транспортные средства TNEF используются для перевода сообщений между системами обмена сообщениями, которые поддерживают различные наборы свойств MAPI.</span><span class="sxs-lookup"><span data-stu-id="176ee-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="176ee-118">ТранспортЫ TNEF используют интерфейс MAPI [ITnef : IUnknown](itnefiunknown.md) для преобразования любых свойств, которые система назначения не может представлять непосредственно в двоичный поток данных, который можно прикрепить к сообщению.</span><span class="sxs-lookup"><span data-stu-id="176ee-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="176ee-119">Позже другой транспорт TNEF может использовать **ITnef** для расшифровки потока данных и сделать исходные свойства MAPI доступными для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="176ee-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="176ee-120">Кроме того, поддержка TNEF необходима, если транспорту необходимо поддерживать настраиваемые классы сообщений.</span><span class="sxs-lookup"><span data-stu-id="176ee-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="176ee-121">Сведения о реализации транспортных средств TNEF см. в TNEF-Enabled [поставщика транспорта.](developing-a-tnef-enabled-transport-provider.md)</span><span class="sxs-lookup"><span data-stu-id="176ee-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="176ee-122">Если поставщик транспорта не является одним из этих типов, вам придется реализовать его с помощью базовых функций MAPI и сетевых функций, доступных на целевой платформе.</span><span class="sxs-lookup"><span data-stu-id="176ee-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

