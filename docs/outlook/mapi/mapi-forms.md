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
ms.openlocfilehash: 951a1c88d2fd4291ee0b48924de6eda8f43c3e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409974"
---
# <a name="mapi-forms"></a><span data-ttu-id="22e61-103">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="22e61-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="22e61-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22e61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22e61-105">После прочтения этого обзора архитектуры форм MAPI вы сможете получить представление о том, какие формы MAPI и как они взаимодействуют с другими компонентами подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="22e61-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="22e61-106">Цель этого раздела — предоставить вам концептуальные знания, необходимые для реализации собственных серверов форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="22e61-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="22e61-107">Перед чтением этого раздела необходимо ознакомиться с материалами в разделе [MapI Forms Overview.](mapi-forms-overview.md)</span><span class="sxs-lookup"><span data-stu-id="22e61-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="22e61-108">Так как архитектура формы MAPI основана на компонентной объектной модели (COM), разработка приложений сервера форм требует знаний о программировании com.</span><span class="sxs-lookup"><span data-stu-id="22e61-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="22e61-109">Дополнительные сведения о com см. в разделе COM и ActiveX object Services в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="22e61-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

