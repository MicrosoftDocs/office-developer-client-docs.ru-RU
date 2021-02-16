---
title: Команды форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: dbd08437dfdd38c3a43cbf12eae8710cc8e3661e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424030"
---
# <a name="form-verbs"></a><span data-ttu-id="c1a0a-103">Команды форм</span><span class="sxs-lookup"><span data-stu-id="c1a0a-103">Form verbs</span></span>

<span data-ttu-id="c1a0a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1a0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1a0a-105">Пользовательский интерфейс формы обычно предлагает элементы меню или элементы управления, которые позволяют пользователям делать какие-либо действия с формой.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="c1a0a-106">Обработка этих действий пользователей на сервере форм является задачей сервера форм.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="c1a0a-107">Этот интерфейс реализуется с помощью стандартных API Win32; Написание одной такой же, как и написание других интерфейсов для обычных программ Win32.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="c1a0a-108">Часто действия пользователя связаны с глаголами.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="c1a0a-109">Глагол — это имя действия, которое является специфическим для определенного класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="c1a0a-110">Например, **reply** — это глагол, реализованный многими серверами форм, каждый из которых может иметь разную интерпретацию этой команды.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="c1a0a-111">Глаголы иногда называют командами.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c1a0a-112">Не все элементы меню и элементы управления в форме соответствуют глаголу.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="c1a0a-113">Например, кнопка **"Отмена"** не соответствует глаголу "Отмена" на сервере формы.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="c1a0a-114">Обычно глаголы связаны с действиями, характерными для определенного класса сообщений или набора классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="c1a0a-115">Хотя разные классы сообщений могут поддерживать разные наборы глаголов, все они поддерживают по крайней мере глагол Open, который отображает пользовательский интерфейс формы и загружает его со значениями свойств сообщения.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="c1a0a-116">Глаголы не могут принимать параметры.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-116">Verbs may take no parameters.</span></span> <span data-ttu-id="c1a0a-117">Формы, которые экспортируют команды с переменными параметрами, должны использовать механизмы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="c1a0a-118">Клиенты могут определить, какие команды поддерживаются определенным классом сообщений, с помощью метода [IMAPIFormInfo::CalcVerbSet,](imapiforminfo-calcverbset.md) который реализуется диспетчером форм MAPI.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="c1a0a-119">Диспетчер форм получает эти сведения из файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="c1a0a-120">Набор глаголов, возвращаемого этим методом, используется клиентом, чтобы показать пользователю, какие команды можно выполнять в сообщении.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="c1a0a-121">Например, клиент может позволить пользователям нажать на сообщение правую кнопку мыши, чтобы отобразить команды, применимые к этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="c1a0a-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1a0a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c1a0a-122">See also</span></span>

- [<span data-ttu-id="c1a0a-123">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a0a-123">MAPI Forms</span></span>](mapi-forms.md)

