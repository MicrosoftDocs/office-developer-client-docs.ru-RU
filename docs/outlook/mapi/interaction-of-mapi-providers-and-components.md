---
title: Взаимодействие поставщиков MAPI и компонентов
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
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="a94ed-103">Взаимодействие поставщиков MAPI и компонентов</span><span class="sxs-lookup"><span data-stu-id="a94ed-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="a94ed-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a94ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a94ed-105">Поставщики службы MAPI любого рода должны следовать определенным рекомендациям для работы с другими компонентами MAPI.</span><span class="sxs-lookup"><span data-stu-id="a94ed-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="a94ed-106">Каждый поставщик услуг должен:</span><span class="sxs-lookup"><span data-stu-id="a94ed-106">Each service provider must:</span></span>
  
- <span data-ttu-id="a94ed-107">Используйте для инициализации нужные объекты provider и logon.</span><span class="sxs-lookup"><span data-stu-id="a94ed-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="a94ed-108">Возвратить таблицу диспетчеризации точек входа поставщика в систему обмена сообщениями после инициализации.</span><span class="sxs-lookup"><span data-stu-id="a94ed-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="a94ed-109">ЗаРегистрируйте строку таблицы состояния MAPI для каждого ресурса, принадлежащего поставщику, и вызовите метод [имаписуппорт:: модифистатусров](imapisupport-modifystatusrow.md) в соответствующее время.</span><span class="sxs-lookup"><span data-stu-id="a94ed-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="a94ed-110">Используйте метод [имаписуппорт:: невуид](imapisupport-newuid.md) для получения допустимых уникальных идентификаторов (UID).</span><span class="sxs-lookup"><span data-stu-id="a94ed-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="a94ed-111">Поддерживает стандартные интерфейсы MAPI для возвращаемых объектов.</span><span class="sxs-lookup"><span data-stu-id="a94ed-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="a94ed-112">Используйте функции выделения памяти MAPI для выделения памяти, возвращаемой клиентским приложениям, и освобождения памяти, выделенной другими частями подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="a94ed-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="a94ed-113">Поддержание раздела профиля, если необходимо, для хранения учетных данных в базовой системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a94ed-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="a94ed-114">Используйте метод [имаписуппорт:: регистерпрепроцессор](imapisupport-registerpreprocessor.md) , чтобы зарегистрировать любые функции предварительной обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="a94ed-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="a94ed-115">Включите соответствующие файлы заголовков (включая маписпи. h), которые определяют общие константы, структуры, интерфейсы и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="a94ed-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="a94ed-116">Используйте соглашения о форматах адресов для распространенных типов адресов.</span><span class="sxs-lookup"><span data-stu-id="a94ed-116">Follow address format conventions for common address types.</span></span>
    

