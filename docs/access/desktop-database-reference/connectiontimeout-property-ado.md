---
title: Свойство ConnectionTimeout (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295704"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="3f7f3-102">Свойство ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="3f7f3-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="3f7f3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f7f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f7f3-104">Указывает, сколько времени нужно подождать, пока будет устанавливаться подключение, прежде чем завершить попытку и создать ошибку.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3f7f3-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3f7f3-105">Settings and return values</span></span>

<span data-ttu-id="3f7f3-106">Задает или возвращает значение **Long,** которое указывает (в секундах) время ожидания открытия подключения.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="3f7f3-107">Значение по умолчанию — 15.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-107">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f7f3-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="3f7f3-108">Remarks</span></span>

<span data-ttu-id="3f7f3-109">Используйте свойство **ConnectionTimeout** объекта [Connection,](connection-object-ado.md) если задержка сетевого трафика или интенсивное использование сервера делают необходимым отказаться от попытки подключения.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-109">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt.</span></span> <span data-ttu-id="3f7f3-110">Если время, задаваемого параметром свойства **ConnectionTimeout** до открытия подключения, уже зависает, возникает ошибка, и ADO отменяет попытку.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-110">If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt.</span></span> <span data-ttu-id="3f7f3-111">Если для свойства установлено нулевое значение, ADO будет ждать неопределенное время, пока не будет открыто подключение.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-111">If you set the property to zero, ADO will wait indefinitely until the connection is opened.</span></span> <span data-ttu-id="3f7f3-112">Убедитесь, что поставщик, которому вы пишете код, поддерживает **функции ConnectionTimeout.**</span><span class="sxs-lookup"><span data-stu-id="3f7f3-112">Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="3f7f3-113">Свойство **ConnectionTimeout** считывать и записывать при закрытии подключения и только для чтения, когда оно открыто.</span><span class="sxs-lookup"><span data-stu-id="3f7f3-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

