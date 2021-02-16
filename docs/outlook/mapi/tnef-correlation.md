---
title: Корреляция TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Дата последнего изменения: 12 марта 2013 г.'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410373"
---
# <a name="tnef-correlation"></a><span data-ttu-id="6b734-103">Корреляция TNEF</span><span class="sxs-lookup"><span data-stu-id="6b734-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="6b734-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b734-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b734-105">Некоторые системы обмена сообщениями выполняют проверку корреляции для любого потока Transport-Neutral TNEF, вложенного в входящие сообщения, чтобы убедиться, что поток TNEF действительно принадлежит этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="6b734-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="6b734-106">Это включает соответствие значения некоторого поля в загоне входящие сообщения с копией этого значения, хранимой в некотором свойстве в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="6b734-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="6b734-107">Для этого обычно используются значения, которые являются уникальными для каждого сообщения, например номера ИД сообщения.</span><span class="sxs-lookup"><span data-stu-id="6b734-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="6b734-108">Транспорт или шлюз, создающий поток TNEF, отвечает за выбор соответствующего значения в загоне сообщения и размещение копии в соответствующем свойстве перед кодизацей свойств исходячего сообщения в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="6b734-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="6b734-109">Затем шлюзы или транспортные средства, получающие сообщение, могут извлечь это свойство из потока TNEF и убедиться, что его значение соответствует значению соответствующего поля в входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="6b734-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="6b734-110">Если значения не совпадают, шлюз или транспорт должны отменить поток TNEF и обработать только конверт сообщения.</span><span class="sxs-lookup"><span data-stu-id="6b734-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="6b734-111">Такие проверки являются целесообразными, так как почтовые клиенты, не относящиеся к MAPI, могут вложите файл, содержащий поток TNEF из старого сообщения в пересылку или даже несвязанные сообщения; Если не проверить, такая ошибка может привести к потере текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="6b734-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="6b734-112">Выбранное значение поля должно быть уникальным для сообщения.</span><span class="sxs-lookup"><span data-stu-id="6b734-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="6b734-113">Для всех систем обмена сообщениями не существует фиксированного поля загона, так как разные системы обмена сообщениями используют разные поля, но обычно система обмена сообщениями назначает сообщению уникальный идентификатор, который подходит для этой цели.</span><span class="sxs-lookup"><span data-stu-id="6b734-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="6b734-114">Например, в системах SMTP обычно используется загодник MessageID, а в системах X.400 IM_THIS_IPM атрибута.</span><span class="sxs-lookup"><span data-stu-id="6b734-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

