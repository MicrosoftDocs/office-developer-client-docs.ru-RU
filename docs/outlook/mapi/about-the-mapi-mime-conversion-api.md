---
title: Сведения об API преобразования MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420439"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="2c61e-103">Сведения об API преобразования MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="2c61e-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="2c61e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c61e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c61e-105">API преобразования MAPI-MIME позволяет почтовым поставщикам выполнять преобразование между объектами MIME и сообщениями MAPI.</span><span class="sxs-lookup"><span data-stu-id="2c61e-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="2c61e-106">Он предоставляет определения констант, идентификаторы классов и идентификаторы интерфейсов, как показано в [константах MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2c61e-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="2c61e-107">Поставщики почты должны создать экземпляр **[иконвертерсессион](iconvertersessioniunknown.md)** , вызвав функцию **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="2c61e-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

