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
# <a name="creating-a-message-subject"></a><span data-ttu-id="754b7-103">Создание темы сообщения</span><span class="sxs-lookup"><span data-stu-id="754b7-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="754b7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="754b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="754b7-105">Тема сообщения, PR_SUBJECT **(** [PidTagSubject),](pidtagsubject-canonical-property.md)является необязательным свойством, используемым для обобщения намерения сообщения.</span><span class="sxs-lookup"><span data-stu-id="754b7-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="754b7-106">Если вы решили установить его, сделайте его строкой символов 128 bytes или меньше.</span><span class="sxs-lookup"><span data-stu-id="754b7-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="754b7-107">Ограничение в 128байт не является ограничением, налагаемом MAPI; это ограничение, накладывается некоторыми поставщиками store сообщений.</span><span class="sxs-lookup"><span data-stu-id="754b7-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="754b7-108">Чтобы обеспечить взаимозаменяемость с поставщиками, которые налагают эту возможность, ограничите количество субъектов до 128байт.</span><span class="sxs-lookup"><span data-stu-id="754b7-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="754b7-109">Следует помнить, что некоторые поставщики store сообщений **не** позволяют PR_SUBJECT в поток с помощью [интерфейса IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="754b7-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="754b7-110">Не **задав PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix);](pidtagsubjectprefix-canonical-property.md) Это свойство устанавливается только для ответов и переададантных сообщений.</span><span class="sxs-lookup"><span data-stu-id="754b7-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

