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
# <a name="internettimeout-property-rds"></a><span data-ttu-id="bbf5b-102">Свойство InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="bbf5b-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="bbf5b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbf5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbf5b-104">Указывает время ожидания (в миллисекундах) до истечения времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="bbf5b-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="bbf5b-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bbf5b-105">Settings and return values</span></span>

<span data-ttu-id="bbf5b-106">Задает или возвращает значение **типа Long** , представляющее количество миллисекунд до истечения времени ожидания для запроса.</span><span class="sxs-lookup"><span data-stu-id="bbf5b-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf5b-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="bbf5b-107">Remarks</span></span>

<span data-ttu-id="bbf5b-108">Это свойство применяется только к запросам, отправляемым с помощью протоколов HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bbf5b-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="bbf5b-109">Выполнение запросов в трехуровневой среде может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="bbf5b-109">Requests in a three-tier environment can take several minutes to execute.</span></span> <span data-ttu-id="bbf5b-110">Используйте это свойство, чтобы указать дополнительное время для долго выполняемых запросов.</span><span class="sxs-lookup"><span data-stu-id="bbf5b-110">Use this property to specify additional time for long-running requests.</span></span>

