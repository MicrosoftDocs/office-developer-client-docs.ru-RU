---
title: Свойство InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1287289de5ef303e41a342ef84822d3a14083470
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918809"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="6a4b4-102">Свойство InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="6a4b4-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="6a4b4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a4b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a4b4-104">Указывает время в миллисекундах для ожидания, по истечении времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="6a4b4-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6a4b4-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6a4b4-105">Settings and return values</span></span>

<span data-ttu-id="6a4b4-106">Задает или возвращает значение типа **Long** , представляющее номер (в миллисекундах) перед запрос будет завершен.</span><span class="sxs-lookup"><span data-stu-id="6a4b4-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a4b4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a4b4-107">Remarks</span></span>

<span data-ttu-id="6a4b4-108">Это свойство применяется только к запросы, отправленные по протоколам HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6a4b4-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="6a4b4-109">Запросы в среде трехуровневой может занять несколько минут для выполнения.</span><span class="sxs-lookup"><span data-stu-id="6a4b4-109">Requests in a three-tier environment can take several minutes to execute.</span></span> <span data-ttu-id="6a4b4-110">Это свойство используется для указания дополнительного времени для длительным запросам.</span><span class="sxs-lookup"><span data-stu-id="6a4b4-110">Use this property to specify additional time for long-running requests.</span></span>

