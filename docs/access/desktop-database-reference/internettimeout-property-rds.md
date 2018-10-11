---
title: InternetTimeout Property (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929b166a308276836fbe4a48a2461ef7eb0caba2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479786"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="bd3b4-102">InternetTimeout Property (RDS)</span><span class="sxs-lookup"><span data-stu-id="bd3b4-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="bd3b4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd3b4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd3b4-104">Указывает время в миллисекундах для ожидания, по истечении времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="bd3b4-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="bd3b4-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bd3b4-105">Settings and Return Values</span></span>

<span data-ttu-id="bd3b4-106">Задает или возвращает значение типа **Long** , представляющее номер (в миллисекундах) перед запрос будет завершен.</span><span class="sxs-lookup"><span data-stu-id="bd3b4-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd3b4-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd3b4-107">Remarks</span></span>

<span data-ttu-id="bd3b4-108">Это свойство применяется только к запросы, отправленные по протоколам HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bd3b4-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="bd3b4-109">Запросы в среде трехуровневой может занять несколько минут для выполнения.</span><span class="sxs-lookup"><span data-stu-id="bd3b4-109">Requests in a three-tier environment can take several minutes to execute.</span></span> <span data-ttu-id="bd3b4-110">Это свойство используется для указания дополнительного времени для длительным запросам.</span><span class="sxs-lookup"><span data-stu-id="bd3b4-110">Use this property to specify additional time for long-running requests.</span></span>

