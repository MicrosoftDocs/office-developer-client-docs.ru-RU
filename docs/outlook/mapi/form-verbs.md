---
title: Форма команд
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a63bf0a7-24e6-4eef-98e8-3744ce5f9f2d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ecc80feec2b0a86f35d03f1ca4f75ea9ff094e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808477"
---
# <a name="form-verbs"></a><span data-ttu-id="e7e40-103">Форма команд</span><span class="sxs-lookup"><span data-stu-id="e7e40-103">Form verbs</span></span>

<span data-ttu-id="e7e40-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7e40-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7e40-105">Пользовательский интерфейс формы обычно предлагает пунктов меню или элементов управления, которые позволяют пользователям выполнить какое-либо действие с формой.</span><span class="sxs-lookup"><span data-stu-id="e7e40-105">A form's user interface typically offers menu items or controls that enable users to take some kind of action with the form.</span></span> <span data-ttu-id="e7e40-106">Это задание сервера формы для обработки этих действий пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7e40-106">It is the form server's job to handle these user actions.</span></span> <span data-ttu-id="e7e40-107">Этот интерфейс реализуется с помощью стандартных интерфейсов API Win32; одну запись — так же, как записи других интерфейсов для регулярного Win32 программы.</span><span class="sxs-lookup"><span data-stu-id="e7e40-107">This interface is implemented using standard Win32 APIs; writing one is just like writing other interfaces for regular Win32 programs.</span></span>
  
<span data-ttu-id="e7e40-108">Часто пользовательских действий связаны с команд.</span><span class="sxs-lookup"><span data-stu-id="e7e40-108">Often, user actions are associated with verbs.</span></span> <span data-ttu-id="e7e40-109">Команды — это имя для действия, характерные для определенного класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7e40-109">A verb is the name for an action that is specific to a certain message class.</span></span> <span data-ttu-id="e7e40-110">Например **ответ** — это команда, реализуемый большое количество серверов формы, каждая из которых может иметь разные интерпретацию этой команды.</span><span class="sxs-lookup"><span data-stu-id="e7e40-110">For example, **Reply** is a verb that is implemented by many form servers, each of which may have a different interpretation of that verb.</span></span> <span data-ttu-id="e7e40-111">Команды иногда называется команды.</span><span class="sxs-lookup"><span data-stu-id="e7e40-111">Verbs are sometimes referred to as commands.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e7e40-112">Не все элементы меню и элементов управления на форме соответствуют команды.</span><span class="sxs-lookup"><span data-stu-id="e7e40-112">Not all menu items and controls on a form correspond to a verb.</span></span> <span data-ttu-id="e7e40-113">Например кнопка **Отмена** не соответствует команда "Отмена" в пределах сервера формы.</span><span class="sxs-lookup"><span data-stu-id="e7e40-113">For example, a **Cancel** button does not correspond to a Cancel verb within the form server.</span></span> <span data-ttu-id="e7e40-114">Как правило команды связаны с действиями, характерные для определенного сообщения класса или набора классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="e7e40-114">Usually, verbs are associated with actions that are specific to a particular message class or a set of message classes.</span></span> <span data-ttu-id="e7e40-115">Хотя для различных классов сообщений может поддерживать различные наборы команд, все по крайней мере поддерживает команду Open, отображает формы пользовательского интерфейса и загружает значения свойства сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7e40-115">Although different message classes can support different sets of verbs, all support at least the Open verb, which displays the form's user interface and loads it with the message's property values.</span></span> 
  
<span data-ttu-id="e7e40-116">Команды может занять без параметров.</span><span class="sxs-lookup"><span data-stu-id="e7e40-116">Verbs may take no parameters.</span></span> <span data-ttu-id="e7e40-117">Формы, которые Экспорт команд с помощью переменной параметры необходимо использовать механизмы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e7e40-117">Forms that export commands with variable parameters must use the Automation mechanisms.</span></span>
  
<span data-ttu-id="e7e40-118">Клиенты можно определить, какие команды поддерживаются классом определенного сообщения через метод [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) , который реализован диспетчера формы MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7e40-118">Clients can determine which verbs are supported by a particular message class through the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method, which is implemented by the MAPI form manager.</span></span> <span data-ttu-id="e7e40-119">Диспетчер форм возвращает эту информацию из файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="e7e40-119">The form manager gets this information from the form's configuration file.</span></span> <span data-ttu-id="e7e40-120">Команда set, возвращаемые данным методом используется клиентом для отображения пользователя, какие команды могут быть выполнены на сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7e40-120">The verb set returned by this method is used by the client to show the user which commands can be executed on a message.</span></span> <span data-ttu-id="e7e40-121">Например клиент может разрешить пользователям щелкните правой кнопкой мыши на сообщение, которое должно отображаться команд, которые применяются к этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7e40-121">For example, a client might enable users to click the right mouse button over a message to display verbs applicable to that message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e7e40-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e7e40-122">See also</span></span>

- [<span data-ttu-id="e7e40-123">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="e7e40-123">MAPI Forms</span></span>](mapi-forms.md)

