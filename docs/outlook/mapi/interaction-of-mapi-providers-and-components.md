---
title: Взаимодействие компонентов и поставщиков MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c0e010b-0432-4ef7-a243-3a4b46f0a19d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c81da7673d6c0c59de6992bc46362069daf71b42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592628"
---
# <a name="interaction-of-mapi-providers-and-components"></a><span data-ttu-id="9fe29-103">Взаимодействие компонентов и поставщиков MAPI</span><span class="sxs-lookup"><span data-stu-id="9fe29-103">Interaction of MAPI Providers and Components</span></span>

  
  
<span data-ttu-id="9fe29-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fe29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fe29-105">Поставщиков служб MAPI никакой должны соответствовать определенным правилам для работы с другими компонентами MAPI.</span><span class="sxs-lookup"><span data-stu-id="9fe29-105">MAPI service providers of any kind must follow certain guidelines to work with other MAPI components.</span></span> <span data-ttu-id="9fe29-106">Каждый поставщик услуг выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9fe29-106">Each service provider must:</span></span>
  
- <span data-ttu-id="9fe29-107">Используйте соответствующие объекты поставщика и входа в систему для инициализации.</span><span class="sxs-lookup"><span data-stu-id="9fe29-107">Use the proper provider and logon objects for initialization.</span></span>
    
- <span data-ttu-id="9fe29-108">Вернуться к системе обмена сообщениями при инициализации бездействия точек входа поставщика.</span><span class="sxs-lookup"><span data-stu-id="9fe29-108">Return a dispatch table of provider entry points to the messaging system upon initialization.</span></span>
    
- <span data-ttu-id="9fe29-109">Зарегистрируйте строки состояния MAPI для каждого ресурса, владельцем которого поставщика и вызовите метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) в соответствующие моменты.</span><span class="sxs-lookup"><span data-stu-id="9fe29-109">Register a MAPI status table row for each resource owned by the provider and call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method at appropriate times.</span></span> 
    
- <span data-ttu-id="9fe29-110">Используйте метод [IMAPISupport::NewUID](imapisupport-newuid.md) для получения допустимого уникальных идентификаторов (UID).</span><span class="sxs-lookup"><span data-stu-id="9fe29-110">Use the [IMAPISupport::NewUID](imapisupport-newuid.md) method to obtain valid unique identifiers (UIDs).</span></span> 
    
- <span data-ttu-id="9fe29-111">Поддерживает общие интерфейсы MAPI на объекты, которые он возвращает.</span><span class="sxs-lookup"><span data-stu-id="9fe29-111">Support the common MAPI interfaces on objects it returns.</span></span>
    
- <span data-ttu-id="9fe29-112">Использование функций выделения памяти MAPI для выделения памяти, возвращаемых для клиентских приложений и для освобождения памяти, выделенной с другими частями подсистемы MAPI.</span><span class="sxs-lookup"><span data-stu-id="9fe29-112">Use the MAPI memory allocation functions to allocate memory returned to client applications and to release memory allocated by other parts of the MAPI subsystem.</span></span>
    
- <span data-ttu-id="9fe29-113">Ведение раздела профилей, если это необходимо для хранения учетных данных для базовой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9fe29-113">Maintain a profile section, if necessary, to store credentials to the underlying messaging system.</span></span>
    
- <span data-ttu-id="9fe29-114">Используйте метод [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) для регистрации любых сообщений о функции предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="9fe29-114">Use the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method to register any message preprocessing functions.</span></span> 
    
- <span data-ttu-id="9fe29-115">Включить соответствующие файлы заголовков (включая mapispi.h), которые определяют распространенные константы, структуры, интерфейсы и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="9fe29-115">Include the proper header files (including mapispi.h) that define common constants, structures, interfaces, and return values.</span></span>
    
- <span data-ttu-id="9fe29-116">Формат соглашениям для распространенных типов адресов адрес.</span><span class="sxs-lookup"><span data-stu-id="9fe29-116">Follow address format conventions for common address types.</span></span>
    

