---
title: Формы MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e3f35126f3887bc1f2979721deb90891b97c9322
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809752"
---
# <a name="mapi-forms"></a><span data-ttu-id="4aa8d-103">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="4aa8d-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="4aa8d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4aa8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4aa8d-105">После прочтения этой Обзор архитектура формы MAPI, будут иметь знания формы MAPI и взаимодействие с другими компонентами в подсистеме MAPI.</span><span class="sxs-lookup"><span data-stu-id="4aa8d-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="4aa8d-106">В этом разделе предназначен для предоставления концептуальные базы знаний, необходимых для реализации серверах формы MAPI.</span><span class="sxs-lookup"><span data-stu-id="4aa8d-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="4aa8d-107">Перед прочтением этого раздела следует ознакомиться с материал в разделе [Общие сведения о формах MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="4aa8d-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4aa8d-108">Поскольку архитектура формы MAPI основано на модели компонентных объектов (COM), разработка форм сервера приложений требует знания программирования COM.</span><span class="sxs-lookup"><span data-stu-id="4aa8d-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="4aa8d-109">Дополнительные сведения о COM обратитесь к разделу COM и службы объект ActiveX в пакете SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="4aa8d-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

