---
title: Отправка между доменами обмена сообщениями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410114"
---
# <a name="sending-across-messaging-domains"></a><span data-ttu-id="0e99b-103">Отправка между доменами обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="0e99b-103">Sending Across Messaging Domains</span></span>

  
  
<span data-ttu-id="0e99b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e99b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e99b-105">Домен обмена сообщениями представляет одну или несколько систем обмена сообщениями, совместно использующих общий формат адреса.</span><span class="sxs-lookup"><span data-stu-id="0e99b-105">A messaging domain represents one or more messaging systems that share a common address format.</span></span> <span data-ttu-id="0e99b-106">Связь между несколькими доменами обмена сообщениями заключается в преобразовании сообщения, отправленного в формате исходного домена обмена сообщениями, в формат конечного домена обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e99b-106">Communication across multiple messaging domains involves translating a message sent in the format of the original messaging domain into the format of the destination messaging domain.</span></span> <span data-ttu-id="0e99b-107">Так как не все форматы адресов совместимы, шлюз необходим для перевода информации об адресе из исходного формата в конечный формат.</span><span class="sxs-lookup"><span data-stu-id="0e99b-107">Because not all address formats are compatible, a gateway is needed to translate the addressing information from the source format into the destination format.</span></span> <span data-ttu-id="0e99b-108">Для обеспечения действительности между доменами обмена сообщениями клиентские приложения хранят важную информацию об адресах в свойствах MAPI.</span><span class="sxs-lookup"><span data-stu-id="0e99b-108">To ensure validity across messaging domains, client applications store important addressing information in MAPI properties.</span></span> <span data-ttu-id="0e99b-109">Кроме того, шлюзы выполняют перевод, изучая свойства, которым требуется перевод, и заменяя их форматом, который может использовать конечный домен обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e99b-109">In addition, gateways perform the translation, examining the properties known to need translation and changing them to a format that the destination messaging domain can use.</span></span>
  
<span data-ttu-id="0e99b-110">Ранее MAPI позволял этим сведениям об адресе быть связанными только с пользователями, составляющими текущий список получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="0e99b-110">Previously, MAPI allowed this addressing information to be associated with only the users who comprise a message's current recipient list.</span></span> <span data-ttu-id="0e99b-111">Свойства, описывающие каждого участника списка получателей, потребовали преобразования шлюза для обеспечения допустимости между доменами обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e99b-111">The properties describing each member of the recipient list underwent the required translation by the gateway to ensure validity across messaging domains.</span></span> <span data-ttu-id="0e99b-112">Однако некоторые приложения требуют, чтобы их сообщения включали сведения о пользователях, которые, возможно, были получателями в будущем, или они никогда не будут получателями.</span><span class="sxs-lookup"><span data-stu-id="0e99b-112">However, some applications require that their messages include addressing information about users that perhaps were recipients in the past, will be recipients in the future, or will never be recipients.</span></span> <span data-ttu-id="0e99b-113">Например, приложения маршрутизации, которые отправляют сообщения в указанном порядке группе пользователей, внедряют сведения об адресах этих пользователей в сообщениях.</span><span class="sxs-lookup"><span data-stu-id="0e99b-113">For example, routing applications, which send messages in a specified order to a group of users, embed addressing information about these users in the messages.</span></span> <span data-ttu-id="0e99b-114">Внедренные сведения обычно включают адрес и тип адреса будущих получателей, а также роли и должности в порядке маршрутизации, их имена и один или несколько двоичных идентификаторов для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="0e99b-114">The embedded information typically includes the address and address type of the future recipients, and perhaps also their roles and positions in the routing order, their names, and one or more binary identifiers per recipient.</span></span>
  
<span data-ttu-id="0e99b-115">Чтобы включить в сообщения сведения об этих неполучателях, MAPI теперь включает стратегию, обеспечивающую правильное преобразование данных о неполучателех в домены обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e99b-115">To enable messages to include information about these nonrecipient users, MAPI now includes a strategy for ensuring that this nonrecipient information is also translated correctly across messaging domains.</span></span> <span data-ttu-id="0e99b-116">Эта стратегия основана на концепции свойств Gateway-сопоставляемые со.</span><span class="sxs-lookup"><span data-stu-id="0e99b-116">This strategy is based on the concept of gateway-mappable properties.</span></span>
  

