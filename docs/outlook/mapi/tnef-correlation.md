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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327400"
---
# <a name="tnef-correlation"></a><span data-ttu-id="f1d66-103">Корреляция TNEF</span><span class="sxs-lookup"><span data-stu-id="f1d66-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="f1d66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1d66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1d66-105">Некоторые системы обмена сообщениями выполняют проверку корреляции для любого потока TNEF, подключенного к входящему сообщению, чтобы убедиться в том, что поток TNEF принадлежит этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="f1d66-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="f1d66-106">Это подразумевает совпадение значения некоторого поля в заголовке входящего сообщения с копией этого значения, хранящейся в свойстве в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="f1d66-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="f1d66-107">Значения, которые предположительно уникальны для каждого сообщения, такие как ИДЕНТИФИКАЦИОНные номера сообщений, обычно используются для этого.</span><span class="sxs-lookup"><span data-stu-id="f1d66-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="f1d66-108">Транспорт или шлюз, который создал поток TNEF, отвечает за выбор подходящего значения из заголовка сообщения и помещение копии в соответствующее свойство, прежде чем кодировать свойства исходящего сообщения в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="f1d66-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="f1d66-109">Шлюзы или транспорты, получающие сообщение, могут затем извлечь это свойство из потока TNEF и проверить, соответствует ли его значение соответствующему полю заголовка в входящем сообщении.</span><span class="sxs-lookup"><span data-stu-id="f1d66-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="f1d66-110">Если значения не совпадают, шлюз или транспорт должны удалить поток TNEF и обработать только конверт встроенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f1d66-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="f1d66-111">Такие проверки поддерживаются, так как почтовые клиенты, использующие не MAPI, могут прикреплять файл, содержащий поток TNEF, из старого сообщения в переадресацию или даже несвязанное сообщение; Если флажок не установлен, такая ошибка может привести к потере текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1d66-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="f1d66-112">Выбранное значение поля заголовка должно быть уникальным для сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1d66-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="f1d66-113">Нет постоянного поля заголовка для всех систем обмена сообщениями, так как разные системы обмена сообщениями используют различные поля заголовков, но обычно система обмена сообщениями назначает уникальный идентификатор для сообщения, которое подходит для этой цели.</span><span class="sxs-lookup"><span data-stu-id="f1d66-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="f1d66-114">Например, в системах SMTP обычно используется заголовок MessageID, а в системах X. 400 обычно используется атрибут ИМ_СИС_ИПМ.</span><span class="sxs-lookup"><span data-stu-id="f1d66-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

