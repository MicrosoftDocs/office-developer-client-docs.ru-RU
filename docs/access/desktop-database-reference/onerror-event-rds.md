---
title: Событие onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712178"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="b2442-102">Событие onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="b2442-102">onError event (RDS)</span></span>

<span data-ttu-id="b2442-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2442-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2442-104">События **onError** вызывается каждый раз, когда возникает ошибка во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="b2442-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2442-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2442-105">Syntax</span></span>

<span data-ttu-id="b2442-106">onError*SCode* *Описание* *источника* *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="b2442-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="b2442-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2442-107">Parameters</span></span>

|<span data-ttu-id="b2442-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b2442-108">Parameter</span></span>|<span data-ttu-id="b2442-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b2442-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b2442-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="b2442-110">*SCode*</span></span> |<span data-ttu-id="b2442-111">Целое число, указывающее код состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="b2442-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="b2442-112">*Описание*</span><span class="sxs-lookup"><span data-stu-id="b2442-112">*Description*</span></span> |<span data-ttu-id="b2442-113">**Строка** , указывающая описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="b2442-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="b2442-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="b2442-114">*Source*</span></span> |<span data-ttu-id="b2442-115">**Строка** , указывающая запроса или команды, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="b2442-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="b2442-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="b2442-116">*CancelDisplay*</span></span> |<span data-ttu-id="b2442-117">**Логическое** значение, которая, в случае присвоено **значение True**, который запрещает отображение в диалоговом окне ошибки.</span><span class="sxs-lookup"><span data-stu-id="b2442-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

