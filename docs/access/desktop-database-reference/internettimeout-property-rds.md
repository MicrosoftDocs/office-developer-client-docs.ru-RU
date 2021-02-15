---
title: Свойство InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291243"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="80094-102">Свойство InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="80094-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="80094-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80094-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80094-104">Указывает время ожидания запроса в миллисекунах.</span><span class="sxs-lookup"><span data-stu-id="80094-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="80094-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="80094-105">Settings and return values</span></span>

<span data-ttu-id="80094-106">Задает или возвращает **длинное** значение, которое представляет количество миллисекунд, прежде чем время и времени запроса не будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="80094-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="80094-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="80094-107">Remarks</span></span>

<span data-ttu-id="80094-108">Это свойство применяется только к запросам, отправленным с помощью протоколов HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="80094-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="80094-109">Выполнение запросов в трехуровневой среде может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="80094-109">Requests in a three-tier environment can take several minutes to execute.</span></span> <span data-ttu-id="80094-110">Это свойство используется для указания дополнительного времени для длительных запросов.</span><span class="sxs-lookup"><span data-stu-id="80094-110">Use this property to specify additional time for long-running requests.</span></span>

