---
title: Личные библиотеки форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 546b45deaa856bbfa002797e491d9b47be0dd34a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581589"
---
# <a name="personal-form-libraries"></a><span data-ttu-id="7ab6f-103">Личные библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="7ab6f-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="7ab6f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ab6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ab6f-105">Как названия, библиотек личных форм содержат формы представлять интерес для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="7ab6f-106">Библиотека личных форм пользователя — это библиотека форм, связанные с хранилищем сообщений по умолчанию, определенный в профиле пользователя; Каждый профиль, установленные на рабочей станции можно использовать хранилища отдельные по умолчанию и, следовательно, библиотеки форм отдельные личные.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="7ab6f-107">Библиотека личных форм может содержать копии форм, которые также содержатся в других библиотеках форм в дополнение к другим форм.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="7ab6f-108">Библиотека личных форм реализована в таблице связанного содержимого в корневой папке в хранилище сообщений по умолчанию пользователя, будет ли, который находится на сервере или локально на рабочей станции пользователя, не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="7ab6f-109">Если хранилище сообщений по умолчанию хранится на рабочей станции пользователя, личных форм библиотекам предлагают повышения производительности, который позволяет приложениям для доступа к формам локально вместо предложенного по сети.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="7ab6f-110">Он также предоставляет форм пользователям доступ работа в автономном режиме, может произойти, если пользователи хотят иметь свои формы с ними на портативные компьютеры и без доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="7ab6f-111">Свойства и базовой реализацией записи Библиотека личных форм включают свойство «Контейнер ID», который определяет основной контейнер, локальной записи должны быть синхронизированы с.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="7ab6f-112">Это может быть идентификатор произвольной папке, которая содержит формы.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="7ab6f-113">Эта функция особенно полезна, если вы используете Диспетчер настраиваемой формы, который поддерживает какую-либо библиотека форм всей организации; Диспетчер форм будет взяла на себя синхронизация форм, хранимые в библиотеке личных форм и библиотека форм всей организации.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="7ab6f-114">Произойдет, вероятно, когда диспетчер форм был загружен, но теоретически может произойти в любое время.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ab6f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7ab6f-115">See also</span></span>



[<span data-ttu-id="7ab6f-116">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="7ab6f-116">MAPI Forms</span></span>](mapi-forms.md)

