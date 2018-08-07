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
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808249"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="d0309-103">Создание темы сообщения</span><span class="sxs-lookup"><span data-stu-id="d0309-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="d0309-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0309-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0309-105">Тема сообщения, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) — это необязательное свойство, используемый для суммирования смыслу сообщение.</span><span class="sxs-lookup"><span data-stu-id="d0309-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="d0309-106">Если выбрано задание его, сделать его строку знаков 128 байт или меньше.</span><span class="sxs-lookup"><span data-stu-id="d0309-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="d0309-107">Ограничение 128 байтов не предела, накладываемого оператором MAPI; Это ограничения, налагаемые некоторых поставщиков хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0309-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="d0309-108">Чтобы обеспечить взаимодействие с поставщиками, указывающие его, ограничьте субъектам 128 байт.</span><span class="sxs-lookup"><span data-stu-id="d0309-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="d0309-109">Обратите внимание, что некоторые поставщики хранения сообщения не разрешать **PR_SUBJECT** для записи потока с помощью интерфейса [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d0309-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="d0309-110">Не используйте **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Это свойство задавать только для ответов и пересылки сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0309-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

