---
title: Сведения об API преобразования MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575268"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="2bb70-103">Сведения об API преобразования MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="2bb70-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="2bb70-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bb70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bb70-105">API преобразования MAPI-MIME позволяет поставщиков почты для преобразования между объектами MIME и сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bb70-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="2bb70-106">Он содержит определения констант, класс идентификаторы и идентификаторы интерфейса, как показано в [Константы MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2bb70-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="2bb70-107">Поставщики почты должен cocreate экземпляр **[IConverterSession](iconvertersessioniunknown.md)** путем вызова функции **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="2bb70-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

