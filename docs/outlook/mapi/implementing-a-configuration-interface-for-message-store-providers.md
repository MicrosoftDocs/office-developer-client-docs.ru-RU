---
title: Реализация интерфейса конфигурации для поставщиков store сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415889"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="b322b-103">Реализация интерфейса конфигурации для поставщиков store сообщений</span><span class="sxs-lookup"><span data-stu-id="b322b-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="b322b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b322b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b322b-105">Поставщики store сообщений необходимы для реализации интерфейса, который позволяет пользователю настроить поставщика для работы с хранилищем сообщений на компьютере этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="b322b-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="b322b-106">Как правило, поставщик службы хранения сообщений настраивается при добавлении поставщика в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="b322b-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="b322b-107">Интерфейс конфигурации поставщика хранилища сообщений обычно обрабатывает такие задачи, как установка имен пользователей и паролей для защищенных хранилищ сообщений, выбор путей к необходимым файлам и создание механизма хранения, который он будет использовать при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b322b-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="b322b-108">Доступ к реализованным интерфейсам конфигурации осуществляется через дополнительные точки входа в DLL поставщика услуг сообщений.</span><span class="sxs-lookup"><span data-stu-id="b322b-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="b322b-109">Дополнительные сведения см. [в подстройки "Настройка службы сообщений".](configuring-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="b322b-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="b322b-110">Интерфейс конфигурации поставщика хранения сообщений — это единственный пользовательский интерфейс, который должен реализовать поставщик.</span><span class="sxs-lookup"><span data-stu-id="b322b-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b322b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b322b-111">See also</span></span>



[<span data-ttu-id="b322b-112">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="b322b-112">Message Store Features</span></span>](message-store-features.md)

