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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710078"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="073fb-102">Свойство InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="073fb-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="073fb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="073fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="073fb-104">Указывает время в миллисекундах для ожидания, по истечении времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="073fb-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="073fb-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="073fb-105">Settings and return values</span></span>

<span data-ttu-id="073fb-106">Задает или возвращает значение типа **Long** , представляющее номер (в миллисекундах) перед запрос будет завершен.</span><span class="sxs-lookup"><span data-stu-id="073fb-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="073fb-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="073fb-107">Remarks</span></span>

<span data-ttu-id="073fb-108">Это свойство применяется только к запросы, отправленные по протоколам HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="073fb-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="073fb-109">Запросы в среде трехуровневой может занять несколько минут для выполнения.</span><span class="sxs-lookup"><span data-stu-id="073fb-109">Requests in a three-tier environment can take several minutes to execute.</span></span> <span data-ttu-id="073fb-110">Это свойство используется для указания дополнительного времени для длительным запросам.</span><span class="sxs-lookup"><span data-stu-id="073fb-110">Use this property to specify additional time for long-running requests.</span></span>

