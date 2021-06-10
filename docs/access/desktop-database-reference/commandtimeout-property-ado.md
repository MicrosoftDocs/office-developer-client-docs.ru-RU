---
title: Свойство CommandTimeout (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296131"
---
# <a name="commandtimeout-property-ado"></a><span data-ttu-id="7f773-102">Свойство CommandTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f773-102">CommandTimeout property (ADO)</span></span>


<span data-ttu-id="7f773-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f773-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f773-104">Указывает, как долго ждать при выполнении команды перед прекращением попытки и созданием ошибки.</span><span class="sxs-lookup"><span data-stu-id="7f773-104">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7f773-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="7f773-105">Settings and return values</span></span>

<span data-ttu-id="7f773-106">Задает или возвращает значение **Long,** которое указывает в секундах, как долго ждать выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="7f773-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for a command to execute.</span></span> <span data-ttu-id="7f773-107">Значение по умолчанию — 30.</span><span class="sxs-lookup"><span data-stu-id="7f773-107">Default is 30.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f773-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f773-108">Remarks</span></span>

<span data-ttu-id="7f773-109">Используйте свойство **CommandTimeout** на объекте [Подключения](connection-object-ado.md) или объекте [Command,](command-object-ado.md) чтобы разрешить отмену вызова метода [Выполнения](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) из-за задержек из-за сетевого трафика или интенсивного использования сервера.</span><span class="sxs-lookup"><span data-stu-id="7f773-109">Use the **CommandTimeout** property on a [Connection](connection-object-ado.md) object or [Command](command-object-ado.md) object to allow the cancellation of an [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method call, due to delays from network traffic or heavy server use.</span></span> <span data-ttu-id="7f773-110">Если интервал, установленный в свойстве **CommandTimeout,** завершается до завершения выполнения команды, возникает ошибка и ADO отменяет команду.</span><span class="sxs-lookup"><span data-stu-id="7f773-110">If the interval set in the **CommandTimeout** property elapses before the command completes execution, an error occurs and ADO cancels the command.</span></span> <span data-ttu-id="7f773-111">Если задать свойство нулю, ADO будет ждать бесконечно, пока завершится выполнение.</span><span class="sxs-lookup"><span data-stu-id="7f773-111">If you set the property to zero, ADO will wait indefinitely until the execution is complete.</span></span> <span data-ttu-id="7f773-112">Убедитесь, что поставщик и источник данных, к которому вы пишете код, поддерживают функциональность **CommandTimeout.**</span><span class="sxs-lookup"><span data-stu-id="7f773-112">Make sure the provider and data source to which you are writing code support the **CommandTimeout** functionality.</span></span>

<span data-ttu-id="7f773-113">Параметр **CommandTimeout** для объекта **Подключения** не влияет на параметр **CommandTimeout** для объекта **Command** на том же **соединении;** то есть свойство **CommandTimeout** объекта **CommandTimeout** не наследует значение значения  **CommandTimeout** объекта Подключения.</span><span class="sxs-lookup"><span data-stu-id="7f773-113">The **CommandTimeout** setting on a **Connection** object has no effect on the **CommandTimeout** setting on a **Command** object on the same **Connection**; that is, the **Command** object's **CommandTimeout** property does not inherit the value of the **Connection** object's **CommandTimeout** value.</span></span>

<span data-ttu-id="7f773-114">В **объекте Подключение** свойство **CommandTimeout** сохраняется после открытия **подключения.**</span><span class="sxs-lookup"><span data-stu-id="7f773-114">On a **Connection** object, the **CommandTimeout** property remains read/write after the **Connection** is opened.</span></span>

