---
title: Инициализация OLE для MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809434"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="841d7-103">Инициализация OLE для MAPI</span><span class="sxs-lookup"><span data-stu-id="841d7-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="841d7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="841d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="841d7-105">При использовании OLE, вызовите функцию OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) для инициализации библиотеки OLE.</span><span class="sxs-lookup"><span data-stu-id="841d7-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="841d7-106">**OleInitialize** инициализирует глобальные данные для сеанса и подготавливает библиотек OLE для приема звонков.</span><span class="sxs-lookup"><span data-stu-id="841d7-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="841d7-107">Сведения о вызовах **OleInitialize**просмотрите пакет SDK для Windows.</span><span class="sxs-lookup"><span data-stu-id="841d7-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

