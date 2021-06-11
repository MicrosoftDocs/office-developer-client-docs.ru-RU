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
# <a name="tnef-correlation"></a><span data-ttu-id="947f4-103">Корреляция TNEF</span><span class="sxs-lookup"><span data-stu-id="947f4-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="947f4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="947f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="947f4-105">Некоторые системы обмена сообщениями выполняют проверку корреляции на любом потоке Transport-Neutral формате инкапсуляции (TNEF), присоединенном к входящий сообщению, чтобы убедиться, что поток TNEF на самом деле принадлежит этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="947f4-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="947f4-106">Это включает соответствие значения некоторого поля в загоне входящие сообщения с копией этого значения, хранимого в некотором свойстве в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="947f4-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="947f4-107">Для этого обычно используются уникальные значения для каждого сообщения, например номера ID сообщений.</span><span class="sxs-lookup"><span data-stu-id="947f4-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="947f4-108">Транспорт или шлюз, создающий поток TNEF, отвечает за выбор соответствующего значения из загона сообщения и размещение копии в соответствующее свойство, прежде чем кодировать свойства исходячего сообщения в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="947f4-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="947f4-109">Шлюзы или транспорты, получающие сообщение, могут извлечь это свойство из потока TNEF и убедиться, что его значение соответствует значению соответствующего поля загона в входящий сообщении.</span><span class="sxs-lookup"><span data-stu-id="947f4-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="947f4-110">Если значения не совпадают, шлюз или транспорт должны отказаться от потока TNEF и обрабатывать только родной конверт сообщения.</span><span class="sxs-lookup"><span data-stu-id="947f4-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="947f4-111">Такие проверки являются разумными, так как почтовые клиенты, не связанные с MAPI, могут прикреплять файл, содержащий поток TNEF из старого сообщения в пересылку или даже не связанное сообщение; если не проверить, такая ошибка может привести к потере текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="947f4-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="947f4-112">Выбранное значение поля загона должно быть уникальным для сообщения.</span><span class="sxs-lookup"><span data-stu-id="947f4-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="947f4-113">Для всех систем обмена сообщениями не существует фиксированного поля загона, так как различные системы обмена сообщениями используют различные поля загона, но обычно система обмена сообщениями назначает уникальный идентификатор сообщению, подходящему для этой цели.</span><span class="sxs-lookup"><span data-stu-id="947f4-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="947f4-114">Например, в smTP-системах обычно используется заглавный заготок MessageID, в то время как системы X.400 обычно используют атрибут IM_THIS_IPM.</span><span class="sxs-lookup"><span data-stu-id="947f4-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

