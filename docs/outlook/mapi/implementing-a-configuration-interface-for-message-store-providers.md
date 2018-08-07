---
title: Реализация интерфейса конфигурации для поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f7151841eef180a78a13ad161d197af783decfb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809270"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="f9914-103">Реализация интерфейса конфигурации для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="f9914-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="f9914-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9914-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9914-105">Поставщики хранилища сообщений не требуется реализовать интерфейс, который позволяет пользователю настраивать поставщика хранилища сообщений на компьютере этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="f9914-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="f9914-106">Как правило при добавлении поставщика хранилища сообщений профиля пользователя в настроен поставщик хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f9914-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="f9914-107">Интерфейс конфигурации поставщика хранилища сообщений обычно выполняет задачи, такие как имена пользователей и пароли для защищенного сообщения хранилищ, Выбор пути к необходимые файлы и создание базовый механизм хранения его будет использоваться, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="f9914-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="f9914-108">Интерфейс конфигурации, который можно реализовать доступен через дополнительные точки входа в DLL поставщика услуг сообщения.</span><span class="sxs-lookup"><span data-stu-id="f9914-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="f9914-109">[Служба сообщений](configuring-a-message-service.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="f9914-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="f9914-110">Интерфейс конфигурации поставщика хранилища сообщений — это единственный пользовательского интерфейса, который должен быть реализован поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f9914-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f9914-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f9914-111">See also</span></span>



[<span data-ttu-id="f9914-112">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="f9914-112">Message Store Features</span></span>](message-store-features.md)

