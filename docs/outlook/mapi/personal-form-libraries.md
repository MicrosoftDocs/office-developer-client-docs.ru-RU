---
title: Библиотеки личных форм
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
# <a name="personal-form-libraries"></a><span data-ttu-id="9cb44-103">Библиотеки личных форм</span><span class="sxs-lookup"><span data-stu-id="9cb44-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="9cb44-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cb44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cb44-105">Как видно из названия, библиотеки личных форм содержат формы, представляющие интерес для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="9cb44-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="9cb44-106">Личная библиотека форм пользователя — это библиотека форм, связанная с хранилищем сообщений по умолчанию, которое определено в профиле пользователя; Каждый профиль, установленный на рабочей станции, может использовать отдельное хранилище по умолчанию и, таким образом, отдельную личную библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="9cb44-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="9cb44-107">Библиотека личных форм может содержать копии форм, которые также содержатся в других библиотеках форм, помимо других форм.</span><span class="sxs-lookup"><span data-stu-id="9cb44-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="9cb44-108">Библиотека личных форм реализована в таблице связанное содержимое корневой папки в хранилище сообщений пользователя по умолчанию, а также в том случае, если она находится на сервере или на локальном компьютере на рабочей станции пользователя.</span><span class="sxs-lookup"><span data-stu-id="9cb44-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="9cb44-109">Если хранилище сообщений пользователя по умолчанию хранится на рабочей станции пользователя, библиотеки личных форм предоставляют повышенную производительность, позволяя приложениям получать доступ к локальным формам, а не по сети.</span><span class="sxs-lookup"><span data-stu-id="9cb44-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="9cb44-110">Кроме того, они позволяют пользователям работать в автономном режиме, что может произойти, когда пользователи хотят использовать формы с ними на портативных компьютерах и без доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="9cb44-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="9cb44-111">Свойства и базовая реализация записей библиотеки личных форм включают свойство Container ID, которое определяет главный контейнер, с которым должна быть синхронизирована локальная запись.</span><span class="sxs-lookup"><span data-stu-id="9cb44-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="9cb44-112">Это может быть идентификатор произвольной папки, содержащей формы.</span><span class="sxs-lookup"><span data-stu-id="9cb44-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="9cb44-113">Это полезно, если вы используете настраиваемый диспетчер форм, который поддерживает некоторые виды библиотек форм в масштабах Организации; Диспетчер форм позаботится о синхронизации форм, хранящихся в библиотеке личных форм и библиотеке форм в масштабе всей Организации.</span><span class="sxs-lookup"><span data-stu-id="9cb44-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="9cb44-114">Это может произойти, если диспетчер форм был загружен, но теоретически может выполняться в любой момент.</span><span class="sxs-lookup"><span data-stu-id="9cb44-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9cb44-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9cb44-115">See also</span></span>



[<span data-ttu-id="9cb44-116">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="9cb44-116">MAPI Forms</span></span>](mapi-forms.md)

