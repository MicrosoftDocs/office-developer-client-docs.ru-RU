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
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317229"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="7d322-103">Инициализация OLE для MAPI</span><span class="sxs-lookup"><span data-stu-id="7d322-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="7d322-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d322-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d322-105">Если вы также используете OLE, вызовите функцию OLE [олеинитиализе](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) для инициализации библиотек OLE.</span><span class="sxs-lookup"><span data-stu-id="7d322-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="7d322-106">**Олеинитиализе** инициализирует глобальные данные для сеанса и подготавливает библиотеки OLE к приему вызовов.</span><span class="sxs-lookup"><span data-stu-id="7d322-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="7d322-107">Сведения о вызове **олеинитиализе**можно найти в пакете Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7d322-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

