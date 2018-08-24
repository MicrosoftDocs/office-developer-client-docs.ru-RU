---
title: Реализация одноразовой таблицы контейнеров
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d468943f84f1d23f1b4b84881e69cee0041a5bae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576598"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="61284-103">Реализация одноразовой таблицы контейнеров</span><span class="sxs-lookup"><span data-stu-id="61284-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="61284-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61284-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61284-105">Для доступа к таблице одноразовых, относящегося к одному из вашего контейнеров, MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера, чтобы открыть свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с **IMAPITable** интерфейс.</span><span class="sxs-lookup"><span data-stu-id="61284-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="61284-106">Контейнера запрос для возврата его одноразовых таблицы при попытке добавить получателя в контейнере клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="61284-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="61284-107">Если контейнер разрешает получателям, ваш поставщик может возвращаются собственная реализация таблицы или вызова [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) для возврата реализации интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="61284-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="61284-108">Набор шаблонов в таблице одноразовых контейнер должны отражаться тип получателей, которые могут содержать конкретным контейнером.</span><span class="sxs-lookup"><span data-stu-id="61284-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="61284-109">Как правило включает один или два шаблоны, шаблоны для создания отдельного пользователя обмена мгновенными сообщениями или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="61284-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="61284-110">Идентификаторы записей для этих шаблонов хранятся в свойства **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) и **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="61284-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="61284-111">Тем не менее контейнеры являются далеко не только следующие типы записей.</span><span class="sxs-lookup"><span data-stu-id="61284-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="61284-112">Они могут содержать других типов получателей или записи без получателя каталоги.</span><span class="sxs-lookup"><span data-stu-id="61284-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

