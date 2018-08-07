---
title: Сохранение часто используемых свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8d4d575-7aa0-4542-91e2-322a6e400551
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a5fa4510f0bcad69bc17b8ac19433f66ec763fba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812170"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="f627e-103">Сохранение часто используемых свойств</span><span class="sxs-lookup"><span data-stu-id="f627e-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="f627e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f627e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f627e-105">Повысить производительность, хранение данных, который принимает время и ресурсы для получения и часто используемых.</span><span class="sxs-lookup"><span data-stu-id="f627e-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="f627e-106">С помощью дополнительной памяти в некоторых случаях может быть лучшим вариантом, повторяющихся запросов.</span><span class="sxs-lookup"><span data-stu-id="f627e-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="f627e-107">Используйте осторожность и осторожность при создании кэш для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="f627e-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="f627e-108">Имейте в виду, что плохо спроектированные кэша может негативно сказаться на производительности.</span><span class="sxs-lookup"><span data-stu-id="f627e-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="f627e-109">К примеру наиболее электронной почты — это клиенты сообщений (IPM) необходимо отображения и откройте поддерева IPM папок количество раз в сеансах типичного.</span><span class="sxs-lookup"><span data-stu-id="f627e-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="f627e-110">Можно повысить производительность, сохраняя идентификаторы записей для каждой из этих папок.</span><span class="sxs-lookup"><span data-stu-id="f627e-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

