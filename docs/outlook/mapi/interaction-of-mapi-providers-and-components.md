---
title: Взаимодействие поставщиков и компонентов MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b88eafcc1ca6be98c5c1e9418072a5cb35f43345
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434664"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="7f313-103">Взаимодействие поставщиков и компонентов MAPI</span><span class="sxs-lookup"><span data-stu-id="7f313-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="7f313-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f313-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f313-105">Поставщики услуг MAPI любого рода должны следовать определенным рекомендациям для работы с другими компонентами MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f313-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="7f313-106">Каждый поставщик услуг должен:</span><span class="sxs-lookup"><span data-stu-id="7f313-106">Each service provider must:</span></span>
  
- <span data-ttu-id="7f313-107">Используйте объекты надлежащего поставщика и логотипа для инициализации.</span><span class="sxs-lookup"><span data-stu-id="7f313-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="7f313-108">Возвращаем таблицу отправки точек входа поставщика в систему обмена сообщениями после инициализации.</span><span class="sxs-lookup"><span data-stu-id="7f313-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="7f313-109">Зарегистрируйте строку таблицы состояния MAPI для каждого ресурса, который принадлежит поставщику, и позвоните по методу [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) в соответствующее время.</span><span class="sxs-lookup"><span data-stu-id="7f313-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="7f313-110">Используйте метод [IMAPISupport::NewUID](imapisupport-newuid.md) для получения действительных уникальных идентификаторов (UID).</span><span class="sxs-lookup"><span data-stu-id="7f313-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="7f313-111">Поддержка общих интерфейсов MAPI для возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="7f313-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="7f313-112">Используйте функции распределения памяти MAPI для выделения памяти, возвращаемой в клиентские приложения, и для выпуска памяти, выделенной другими частями подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="7f313-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="7f313-113">При необходимости сохраните раздел профилей для хранения учетных данных в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7f313-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="7f313-114">Используйте [метод IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) для регистрации любых функций подготовки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7f313-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="7f313-115">Включаем соответствующие файлы заголовки (в том числе mapispi.h), которые определяют общие константы, структуры, интерфейсы и значения возврата.</span><span class="sxs-lookup"><span data-stu-id="7f313-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="7f313-116">Следуйте конвенциям формата адресов для общих типов адресов.</span><span class="sxs-lookup"><span data-stu-id="7f313-116">Follow address format conventions for common address types.</span></span>
    

