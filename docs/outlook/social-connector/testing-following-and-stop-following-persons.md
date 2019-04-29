---
title: Тестирование подписки на пользователей и ее отмены
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: В этом разделе описываются сценарии, позволяющие протестировать способность поставщика Outlook Social Connector (OSC) подписаться другу и прекратить отслеживание друга в социальной сети.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432452"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="e9fc6-103">Тестирование подписки на пользователей и ее отмены</span><span class="sxs-lookup"><span data-stu-id="e9fc6-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="e9fc6-104">В этом разделе описываются сценарии, позволяющие протестировать способность поставщика Outlook Social Connector (OSC) подписаться другу и прекратить отслеживание друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="e9fc6-105">Отслеживание пользователя</span><span class="sxs-lookup"><span data-stu-id="e9fc6-105">Following a person</span></span>

<span data-ttu-id="e9fc6-106">Чтобы подписаться на человека, добавьте пользователя в качестве друга в социальной сети, используя SMTP-адрес, предоставленный выбранным элементом Outlook.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="e9fc6-107">Следующий пользователь в социальной сети обычно запрашивает разрешение от этого пользователя по электронной почте на этот SMTP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="e9fc6-108">Чтобы предоставить разрешение, необходимо, чтобы этот адрес SMTP уже включался в свою учетную запись социальных сетей или чтобы добавить этот SMTP-адрес в учетную запись социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="e9fc6-109">ПроТестируйте каждый из следующих сценариев, чтобы убедиться, что поставщик OSC работает правильно.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="e9fc6-110">**Сценарий**</span><span class="sxs-lookup"><span data-stu-id="e9fc6-110">**Scenario**</span></span>|<span data-ttu-id="e9fc6-111">**Ожидаемое поведение**</span><span class="sxs-lookup"><span data-stu-id="e9fc6-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9fc6-112">Попытка подписаться на пользователя в социальной сети, который существует в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="e9fc6-113">Для социальных сетей, которые не требуют разрешения у человека, социальные сети немедленно добавляет пользователя в качестве друга.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="e9fc6-114">Для сети, для которой требуется разрешение у этого пользователя, в социальной сети отправляется уведомление.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="e9fc6-115">В области пользователи Outlook отображается значок ожидающих действий для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="e9fc6-116">Попытка подписаться на пользователя в социальной сети, который не существует в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="e9fc6-117">Поставщик OSC отображает соответствующую ошибку в [настроенный ISocialSession:: фолловперсон](isocialsession-followperson.md) или [ISocialSession2:: фолловперсонекс](isocialsession2-followpersonex.md).</span><span class="sxs-lookup"><span data-stu-id="e9fc6-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="e9fc6-118">После друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="e9fc6-119">Для друга, выбранного в области люди, отображаются эмблема социальных сетей и рисунок профиля друга для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="e9fc6-120">Выбор ссылки на страницу профиля друга.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="e9fc6-121">Страница друга в социальной сети открывается в браузере пользователя, вошедшего в систему по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="e9fc6-122">Прекратить отслеживание человека</span><span class="sxs-lookup"><span data-stu-id="e9fc6-122">Stop following a person</span></span>

<span data-ttu-id="e9fc6-123">Чтобы прекратить отслеживание действий пользователя, необходимо удалить этого пользователя в социальной сети в качестве друга.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="e9fc6-124">ПроТестируйте следующий сценарий, чтобы проверить, что поставщик OSC перестает правильно работать после пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="e9fc6-125">**Сценарий**</span><span class="sxs-lookup"><span data-stu-id="e9fc6-125">**Scenario**</span></span>|<span data-ttu-id="e9fc6-126">**Ожидаемое поведение**</span><span class="sxs-lookup"><span data-stu-id="e9fc6-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e9fc6-127">Попытка удалить пользователя в качестве друга в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="e9fc6-128">Социальные сети больше не перечислеают этого человека в учетной записи пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="e9fc6-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9fc6-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e9fc6-129">See also</span></span>

- [<span data-ttu-id="e9fc6-130">Подготовка к выПуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="e9fc6-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

