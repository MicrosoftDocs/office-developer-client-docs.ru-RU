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
ms.openlocfilehash: a9bba55b585b09d6a5779ba41a283b20c645656f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576234"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="07aa6-103">Типы поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="07aa6-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="07aa6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07aa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07aa6-105">Все поставщики транспорта поддерживают диапазон стандартные элементы, такие как:</span><span class="sxs-lookup"><span data-stu-id="07aa6-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="07aa6-106">Предоставление соответствующих прав безопасности для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="07aa6-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="07aa6-107">Отправки и получения сообщений из системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="07aa6-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="07aa6-108">Предоставление типов адресов поставщиками транспорта поддерживают поэтому диспетчер очереди MAPI и клиентские приложения могут использовать их соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="07aa6-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="07aa6-109">Принятие доставки для конкретных получателей.</span><span class="sxs-lookup"><span data-stu-id="07aa6-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="07aa6-110">В дополнение к этому MAPI поддерживает два типа специальных поставщиков для конкретных систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="07aa6-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="07aa6-111">**Тип транспорта**</span><span class="sxs-lookup"><span data-stu-id="07aa6-111">**Transport type**</span></span>|<span data-ttu-id="07aa6-112">**Дополнительные функции**</span><span class="sxs-lookup"><span data-stu-id="07aa6-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07aa6-113">Удаленный транспорта</span><span class="sxs-lookup"><span data-stu-id="07aa6-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="07aa6-114">Делает возможным взаимодействие с клиентами, подключенных удаленно.</span><span class="sxs-lookup"><span data-stu-id="07aa6-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="07aa6-115">Формат TNEF транспорта</span><span class="sxs-lookup"><span data-stu-id="07aa6-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="07aa6-116">Позволяет свойства MAPI, сохраняется, которые не поддерживают системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="07aa6-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="07aa6-117">Транспортов TNEF используются для преобразования сообщений между систем обмена сообщениями, которые поддерживают различные наборы свойств MAPI.</span><span class="sxs-lookup"><span data-stu-id="07aa6-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="07aa6-118">Используйте TNEF транспортов MAPI [ITnef: IUnknown](itnefiunknown.md) интерфейс для преобразования всех свойств, которые не может представлять системы назначения непосредственно в поток двоичных данных, который может быть вложения в сообщение.</span><span class="sxs-lookup"><span data-stu-id="07aa6-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="07aa6-119">Более поздних версий другой транспорта TNEF можно использовать **ITnef** для декодирования потока данных и сделать доступным для клиентских приложений исходного свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="07aa6-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="07aa6-120">Кроме того поддержке формата TNEF является обязательным, если ваше транспорта должна поддерживать настраиваемые классы сообщения.</span><span class="sxs-lookup"><span data-stu-id="07aa6-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="07aa6-121">Сведения о реализации транспортов TNEF просмотрите [Разработка поставщика транспорта TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="07aa6-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="07aa6-122">Если ваш поставщик транспорта не один из этих типов, необходимо реализовать с помощью основных функций MAPI и сетевые функции, доступные на целевой платформы.</span><span class="sxs-lookup"><span data-stu-id="07aa6-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

