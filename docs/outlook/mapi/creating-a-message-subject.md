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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395688"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="40631-103">Создание темы сообщения</span><span class="sxs-lookup"><span data-stu-id="40631-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="40631-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40631-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40631-105">Тема сообщения, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) — это необязательное свойство, используемый для суммирования смыслу сообщение.</span><span class="sxs-lookup"><span data-stu-id="40631-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="40631-106">Если выбрано задание его, сделать его строку знаков 128 байт или меньше.</span><span class="sxs-lookup"><span data-stu-id="40631-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="40631-107">Ограничение 128 байтов не предела, накладываемого оператором MAPI; Это ограничения, налагаемые некоторых поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="40631-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="40631-108">Чтобы обеспечить взаимодействие с поставщиками, указывающие его, ограничьте субъектам 128 байт.</span><span class="sxs-lookup"><span data-stu-id="40631-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="40631-109">Обратите внимание, что некоторые поставщики хранения сообщения не разрешать **PR_SUBJECT** для записи потока с помощью интерфейса [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="40631-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="40631-110">Не используйте **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Это свойство задавать только для ответов и пересылки сообщений.</span><span class="sxs-lookup"><span data-stu-id="40631-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

