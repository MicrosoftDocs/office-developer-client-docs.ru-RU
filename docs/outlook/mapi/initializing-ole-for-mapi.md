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
ms.openlocfilehash: cd279c17574ce73b42d5e07e96ac817af71dc700
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589807"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="df64c-103">Инициализация OLE для MAPI</span><span class="sxs-lookup"><span data-stu-id="df64c-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="df64c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df64c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df64c-105">При использовании OLE, вызовите функцию OLE [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) для инициализации библиотеки OLE.</span><span class="sxs-lookup"><span data-stu-id="df64c-105">If you also use OLE, call the OLE function [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="df64c-106">**OleInitialize** инициализирует глобальные данные для сеанса и подготавливает библиотек OLE для приема звонков.</span><span class="sxs-lookup"><span data-stu-id="df64c-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="df64c-107">Сведения о вызовах **OleInitialize**просмотрите пакет SDK для Windows.</span><span class="sxs-lookup"><span data-stu-id="df64c-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

