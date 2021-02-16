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
ms.openlocfilehash: e32ed3388e95d32a4857a933fb735d170dd71688
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424555"
---
# <a name="saving-frequently-used-properties"></a><span data-ttu-id="02dee-103">Сохранение часто используемых свойств</span><span class="sxs-lookup"><span data-stu-id="02dee-103">Saving Frequently Used Properties</span></span>

  
  
<span data-ttu-id="02dee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02dee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02dee-105">Повышение производительности за счет хранения данных, для получения и частого доступа к ним требуется время и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="02dee-105">Improve performance by storing data that takes time and resources to retrieve and is accessed frequently.</span></span> <span data-ttu-id="02dee-106">Использование дополнительной памяти иногда может быть более лучшим вариантом, когда повторялись повторы.</span><span class="sxs-lookup"><span data-stu-id="02dee-106">Using extra memory can sometimes be a better option that repeated retrievals.</span></span> <span data-ttu-id="02dee-107">При создании кэша для хранения этих данных следует соблюдать осторожность и осторожность.</span><span class="sxs-lookup"><span data-stu-id="02dee-107">Use caution and care when creating a cache for storing this data.</span></span> <span data-ttu-id="02dee-108">Помните, что плохо разработанный кэш может отрицательно сказаться на производительности.</span><span class="sxs-lookup"><span data-stu-id="02dee-108">Keep in mind that a poorly designed cache can negatively impact performance.</span></span>
  
<span data-ttu-id="02dee-109">Например, большинству клиентов межличностных сообщений (IPM) необходимо много раз отобразить и открыть поддереть IPM папок во время типичного сеанса.</span><span class="sxs-lookup"><span data-stu-id="02dee-109">For example, most interpersonal message (IPM) clients need to display and open the IPM subtree of folders many times during a typical session.</span></span> <span data-ttu-id="02dee-110">Для повышения производительности можно хранить идентификаторы записей для каждой из этих папок.</span><span class="sxs-lookup"><span data-stu-id="02dee-110">You can improve performance by storing the entry identifiers for each of these folders.</span></span> 
  

