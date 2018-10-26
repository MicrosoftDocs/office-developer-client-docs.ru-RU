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
ms.openlocfilehash: 15833768fbd148ae4e689b5a80ed3479823864cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592929"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="b2786-103">Реализация интерфейса конфигурации для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="b2786-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="b2786-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2786-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2786-105">Поставщики хранилища сообщений не требуется реализовать интерфейс, который позволяет пользователю настраивать поставщика хранилища сообщений на компьютере этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b2786-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="b2786-106">Как правило при добавлении поставщика хранилища сообщений профиля пользователя в настроен поставщик хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2786-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="b2786-107">Интерфейс конфигурации поставщика хранилища сообщений обычно выполняет задачи, такие как имена пользователей и пароли для защищенного сообщения хранилищ, Выбор пути к необходимые файлы и создание базовый механизм хранения его будет использоваться, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="b2786-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="b2786-108">Интерфейс конфигурации, который можно реализовать доступен через дополнительные точки входа в DLL поставщика услуг сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2786-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="b2786-109">[Служба сообщений](configuring-a-message-service.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="b2786-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="b2786-110">Интерфейс конфигурации поставщика хранилища сообщений — это единственный пользовательского интерфейса, который должен быть реализован поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2786-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2786-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b2786-111">See also</span></span>



[<span data-ttu-id="b2786-112">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="b2786-112">Message Store Features</span></span>](message-store-features.md)

