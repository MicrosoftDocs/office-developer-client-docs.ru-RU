---
title: Библиотеки личной формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420411"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="9a3e2-103">Библиотеки личной формы</span><span class="sxs-lookup"><span data-stu-id="9a3e2-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="9a3e2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a3e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a3e2-105">Как предполагает его имя, библиотеки личной формы содержат формы, интересуя конкретного пользователя.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="9a3e2-106">Библиотека личной формы пользователя — это библиотека форм, связанная с хранилищем сообщений по умолчанию, идентифицированным в профиле пользователя; Каждый профиль, установленный на рабочей станции, может использовать отдельный магазин по умолчанию и, следовательно, отдельную личную библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="9a3e2-107">Библиотека личной формы может содержать копии форм, которые также содержатся в других библиотеках форм в дополнение к другим формам.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="9a3e2-108">Личная библиотека форм реализуется в таблице со связанным содержимым корневой папки в хранилище сообщений пользователя по умолчанию — независимо от того, находится ли она на сервере или локально на рабочей станции пользователя, не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="9a3e2-109">Если хранилище сообщений пользователя по умолчанию хранится на рабочей станции пользователя, библиотеки личной формы обеспечивают повышенную производительность, позволяя приложениям получать доступ к формам локально, а не по сети.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="9a3e2-110">Это также делает формы доступными для пользователей, работающих в автономном режиме, которые могут возникать, когда пользователи хотят взять их формы с собой на портативных компьютерах и не имеют доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="9a3e2-111">Свойства и основные элементы реализации записей библиотеки личной формы включают свойство "Container ID", которое идентифицирует мастер-контейнер, с котором должна синхронизироваться локализованная запись.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="9a3e2-112">Это может быть идентификатор произвольной папки, которая содержит формы.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="9a3e2-113">Это полезно, если используется настраиваемый диспетчер форм, который поддерживает какую-либо библиотеку форм по всей организации; руководитель форм будет заботиться о синхронизации форм, хранимых в личной библиотеке форм и библиотеке форм для всей организации.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="9a3e2-114">Возможно, это произойдет при загрузке диспетчера форм, но теоретически это может произойти в любое время.</span><span class="sxs-lookup"><span data-stu-id="9a3e2-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a3e2-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9a3e2-115">See also</span></span>



[<span data-ttu-id="9a3e2-116">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="9a3e2-116">MAPI Forms</span></span>](mapi-forms.md)

