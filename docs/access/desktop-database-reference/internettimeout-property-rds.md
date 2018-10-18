---
title: InternetTimeout Property (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd0fdc8f64207e1233ac56812ef009da865ce01a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603464"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="83d24-102">InternetTimeout Property (RDS)</span><span class="sxs-lookup"><span data-stu-id="83d24-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="83d24-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="83d24-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="83d24-104">Указывает время в миллисекундах для ожидания, по истечении времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="83d24-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

<span data-ttu-id="83d24-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="83d24-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="83d24-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="83d24-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="83d24-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="83d24-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="83d24-108">master</span><span class="sxs-lookup"><span data-stu-id="83d24-108">master</span></span>

<span data-ttu-id="83d24-109">Задает или возвращает значение типа **Long** , представляющее номер (в миллисекундах) перед запрос будет завершен.</span><span class="sxs-lookup"><span data-stu-id="83d24-109">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="83d24-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="83d24-110">Remarks</span></span>

<span data-ttu-id="83d24-111">Это свойство применяется только к запросы, отправленные по протоколам HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="83d24-111">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="83d24-112">Запросы в среде трехуровневой может занять несколько минут для выполнения.</span><span class="sxs-lookup"><span data-stu-id="83d24-112">Requests in a three-tier environment can take several minutes to execute.</span></span> <span data-ttu-id="83d24-113">Это свойство используется для указания дополнительного времени для длительным запросам.</span><span class="sxs-lookup"><span data-stu-id="83d24-113">Use this property to specify additional time for long-running requests.</span></span>

