---
title: Создание темы сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332965"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="a24a6-103">Создание темы сообщения</span><span class="sxs-lookup"><span data-stu-id="a24a6-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="a24a6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a24a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a24a6-105">Тема сообщения, **PR_SUBJECT** [(PidTagSubject),](pidtagsubject-canonical-property.md)является необязательным свойством, используемым для обобщения намерения сообщения.</span><span class="sxs-lookup"><span data-stu-id="a24a6-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="a24a6-106">Если вы решите установить его, сделайте его строкой символов 128 bytes или меньше.</span><span class="sxs-lookup"><span data-stu-id="a24a6-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="a24a6-107">Ограничение в 128 byte не является ограничением, введенным MAPI; это ограничение, введенное некоторыми поставщиками магазинов сообщений.</span><span class="sxs-lookup"><span data-stu-id="a24a6-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="a24a6-108">Для обеспечения связи с поставщиками, которые налагают его, ограничите количество субъектов 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="a24a6-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="a24a6-109">Следует помнить, что некоторые поставщики  хранения сообщений не позволяют PR_SUBJECT в поток с интерфейсом [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a24a6-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="a24a6-110">Не **задай PR_SUBJECT_PREFIX** [(PidTagSubjectPrefix);](pidtagsubjectprefix-canonical-property.md) это свойство задалось только для ответов и переададных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a24a6-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

