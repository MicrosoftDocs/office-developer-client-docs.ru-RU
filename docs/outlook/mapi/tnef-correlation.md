---
title: Корреляция TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Последнее изменение: 12 марта 2013 г.'
ms.openlocfilehash: b8b30dcc2fcf0c8e75004e36b6fd9f4f4583e304
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812491"
---
# <a name="tnef-correlation"></a><span data-ttu-id="a1708-103">Корреляция TNEF</span><span class="sxs-lookup"><span data-stu-id="a1708-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="a1708-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1708-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1708-105">Некоторые системы обмена сообщениями выполнить проверку корреляции для любой поток Transport-Neutral Encapsulation формата TNEF (), подключенного к входящее сообщение, чтобы убедиться, что поток TNEF фактически принадлежат этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1708-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="a1708-106">Этот подход включает сопоставления значения некоторые поля в заголовке входящее сообщение с копию этого значения, хранящиеся в некоторые свойства в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="a1708-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="a1708-107">Значения, которые являются предположительно уникальными для каждого сообщения, такие как идентификаторы сообщения, обычно используется для данного.</span><span class="sxs-lookup"><span data-stu-id="a1708-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="a1708-108">Транспорта или шлюз, которые созданы в потоке TNEF несет ответственность за Выбор подходящего значения из заголовка сообщения и помещает копию в соответствующее свойство перед Кодировка исходящих сообщений свойства в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="a1708-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="a1708-109">Шлюзы или транспортов, отображается сообщение можно извлечь свойства в потоке TNEF и убедитесь, что его значение соответствует значению поля заголовка для входящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1708-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="a1708-110">Если значения не совпадают, шлюза или транспортного необходимо отменить поток TNEF и процесс только конверт собственные сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1708-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="a1708-111">Такие проверки рациональное, так как не является приложением MAPI почтовые клиенты могут вложить файл, содержащий поток TNEF из старого сообщения для пересылки или даже несвязанных сообщения; Если флажок не установлен, такая ошибка может привести к потере текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1708-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="a1708-112">Значение поля заголовка, выбранное должно быть уникальным в сообщение.</span><span class="sxs-lookup"><span data-stu-id="a1708-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="a1708-113">Нет фиксированной заголовок поля для всех систем обмена сообщениями из-за различных систем обмена сообщениями использование различных заголовков полей, но обычно системы обмена сообщениями назначает уникальный идентификатор сообщения, которая подходит для этой цели.</span><span class="sxs-lookup"><span data-stu-id="a1708-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="a1708-114">Например SMTP систем обычно используется заголовок MessageID во время X.400 систем, как правило, используется атрибут IM_THIS_IPM.</span><span class="sxs-lookup"><span data-stu-id="a1708-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

