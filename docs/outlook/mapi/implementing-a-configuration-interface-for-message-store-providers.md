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
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332979"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="68305-103">Реализация интерфейса конфигурации для поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="68305-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="68305-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68305-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68305-105">Поставщики хранилища сообщений необходимы для реализации интерфейса, который позволяет пользователю настраивать поставщик хранилища сообщений для запуска на компьютере этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="68305-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="68305-106">Как правило, поставщик хранилища сообщений настраивается при добавлении поставщика хранилища сообщений в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="68305-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="68305-107">Интерфейс конфигурации поставщика хранилища сообщений обычно обрабатывает такие задачи, как установка имен пользователей и паролей для защищенных хранилищ сообщений, выбор путей к необходимым файлам и создание используемого механизма хранения, который он будет использовать при необходимости.</span><span class="sxs-lookup"><span data-stu-id="68305-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="68305-108">Доступ к интерфейсу конфигурации, который вы реализуете, осуществляется с помощью дополнительных точек входа в DLL поставщика службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="68305-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="68305-109">Дополнительную информацию можно узнать в статье [Настройка службы сообщений](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="68305-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="68305-110">Интерфейс настройки поставщика хранилища сообщений является единственным пользовательским интерфейсом, который должен быть реализован поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="68305-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68305-111">См. также</span><span class="sxs-lookup"><span data-stu-id="68305-111">See also</span></span>



[<span data-ttu-id="68305-112">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="68305-112">Message Store Features</span></span>](message-store-features.md)

