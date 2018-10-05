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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388420"
---
# <a name="initializing-ole-for-mapi"></a><span data-ttu-id="4fc05-103">Инициализация OLE для MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc05-103">Initializing OLE for MAPI</span></span>

  
  
<span data-ttu-id="4fc05-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fc05-105">При использовании OLE, вызовите функцию OLE [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) для инициализации библиотеки OLE.</span><span class="sxs-lookup"><span data-stu-id="4fc05-105">If you also use OLE, call the OLE function [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) to initialize the OLE libraries.</span></span> <span data-ttu-id="4fc05-106">**OleInitialize** инициализирует глобальные данные для сеанса и подготавливает библиотек OLE для приема звонков.</span><span class="sxs-lookup"><span data-stu-id="4fc05-106">**OleInitialize** initializes global data for the session and prepares the OLE libraries to accept calls.</span></span> <span data-ttu-id="4fc05-107">Сведения о вызовах **OleInitialize**просмотрите пакет SDK для Windows.</span><span class="sxs-lookup"><span data-stu-id="4fc05-107">For information about calling **OleInitialize**, see the Windows SDK.</span></span>
  

