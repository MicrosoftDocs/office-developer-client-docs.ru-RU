---
title: Тестирование подписки на пользователей и ее отмены
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: В этом разделе описаны сценарии, чтобы проверить возможность поставщика Outlook Social Connector (OSC) для подписки друга, а также отменить подписку друга в социальных сетях.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812832"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="373e3-103">Тестирование подписки на пользователей и ее отмены</span><span class="sxs-lookup"><span data-stu-id="373e3-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="373e3-104">В этом разделе описаны сценарии, чтобы проверить возможность поставщика Outlook Social Connector (OSC) для подписки друга, а также отменить подписку друга в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="373e3-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="373e3-105">Отслеживание человека</span><span class="sxs-lookup"><span data-stu-id="373e3-105">Following a person</span></span>

<span data-ttu-id="373e3-106">Для выполнения человеком заключается в добавлении человеком как friend в социальных сетях, с помощью SMTP-адреса, предоставленные выбранный элемент Outlook.</span><span class="sxs-lookup"><span data-stu-id="373e3-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="373e3-107">Отслеживание кто-то на социальной сети обычно включает в себя запроса разрешения от этого лица, сообщение электронной почты на этот адрес SMTP.</span><span class="sxs-lookup"><span data-stu-id="373e3-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="373e3-108">Для предоставления разрешений, он необходимо иметь SMTP-адрес, уже включены в свою учетную запись социальной сети или будет готов для добавления этого SMTP для учетной записи социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="373e3-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="373e3-109">Тестирование каждого из следующих сценариев, чтобы проверить, правильно работает поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="373e3-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="373e3-110">**Сценарий**</span><span class="sxs-lookup"><span data-stu-id="373e3-110">**Scenario**</span></span>|<span data-ttu-id="373e3-111">**Ожидаемое поведение**</span><span class="sxs-lookup"><span data-stu-id="373e3-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="373e3-112">Попытка выполните человека в социальных сетях, находящийся в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="373e3-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="373e3-113">В социальных сетях, не требуются разрешения от лица социальные сети сразу же добавляет пользователя в качестве друга.</span><span class="sxs-lookup"><span data-stu-id="373e3-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="373e3-114">Для сети, который требует разрешения от этого лица социальные сети отправляет уведомление.</span><span class="sxs-lookup"><span data-stu-id="373e3-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="373e3-115">Области пользователей Outlook отображает ожидающие значок этого контакта.</span><span class="sxs-lookup"><span data-stu-id="373e3-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="373e3-116">Попытка выполните человека в социальных сетях, кто не существует в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="373e3-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="373e3-117">Поставщика OSC отображает соответствующие ошибки в [ISocialSession::FollowPerson](isocialsession-followperson.md) или [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span><span class="sxs-lookup"><span data-stu-id="373e3-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="373e3-118">Отслеживание друг на социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="373e3-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="373e3-119">Для friend, выбранного в области пользователей отображаются значка социальной сети и изображение профиля другого пользователя для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="373e3-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="373e3-120">Выбор ссылки на странице профиля друга.</span><span class="sxs-lookup"><span data-stu-id="373e3-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="373e3-121">Откроется страница другого пользователя в социальных сетях в браузере по умолчанию при входе пользователя.</span><span class="sxs-lookup"><span data-stu-id="373e3-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="373e3-122">Прекратить отслеживание человека</span><span class="sxs-lookup"><span data-stu-id="373e3-122">Stop following a person</span></span>

<span data-ttu-id="373e3-123">Чтобы остановить отслеживание человека является удалите его как friend в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="373e3-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="373e3-124">Проверьте следующий сценарий для проверки вашей останавливает поставщика OSC отслеживание человека должным образом.</span><span class="sxs-lookup"><span data-stu-id="373e3-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="373e3-125">**Сценарий**</span><span class="sxs-lookup"><span data-stu-id="373e3-125">**Scenario**</span></span>|<span data-ttu-id="373e3-126">**Ожидаемое поведение**</span><span class="sxs-lookup"><span data-stu-id="373e3-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="373e3-127">Попытка удаления пользователя как friend в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="373e3-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="373e3-128">Социальные сети больше не перечислены он как friend для учетной записи пользователя, выполнившего вход.</span><span class="sxs-lookup"><span data-stu-id="373e3-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="373e3-129">См. также</span><span class="sxs-lookup"><span data-stu-id="373e3-129">See also</span></span>

- [<span data-ttu-id="373e3-130">Подготовка к выпуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="373e3-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

