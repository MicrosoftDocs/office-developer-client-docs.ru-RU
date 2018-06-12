---
title: О преобразовании MAPI-MIME API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807985"
---
# <a name="about-the-mapi-mime-conversion-api"></a><span data-ttu-id="05031-103">О преобразовании MAPI-MIME API</span><span class="sxs-lookup"><span data-stu-id="05031-103">About the MAPI-MIME Conversion API</span></span>

  
  
<span data-ttu-id="05031-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05031-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05031-105">API преобразования MAPI-MIME позволяет поставщиков почты для преобразования между объектами MIME и сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="05031-105">The MAPI-MIME Conversion API allows mail providers to convert between MIME objects and MAPI messages.</span></span> <span data-ttu-id="05031-106">Он содержит определения констант, класс идентификаторы и идентификаторы интерфейса, как показано в [Константы MAPI](mapi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="05031-106">It provides constant definitions, class identifiers, and interface identifiers as shown in [MAPI Constants](mapi-constants.md).</span></span> <span data-ttu-id="05031-107">Поставщики почты должен cocreate экземпляр **[IConverterSession](iconvertersessioniunknown.md)** путем вызова функции **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="05031-107">Mail providers must cocreate an instance of **[IConverterSession](iconvertersessioniunknown.md)** by calling the **CoCreateInstance** function.</span></span> 
  

