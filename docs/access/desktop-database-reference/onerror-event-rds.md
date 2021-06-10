---
title: onError event (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288478"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="74d90-102">onError event (RDS)</span><span class="sxs-lookup"><span data-stu-id="74d90-102">onError event (RDS)</span></span>

<span data-ttu-id="74d90-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74d90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74d90-104">Событие **onError** называется всякий раз, когда во время операции возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="74d90-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="74d90-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74d90-105">Syntax</span></span>

<span data-ttu-id="74d90-106">onError *SCode*, *Описание*, *Источник*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="74d90-106">onError *SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="74d90-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="74d90-107">Parameters</span></span>

|<span data-ttu-id="74d90-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="74d90-108">Parameter</span></span>|<span data-ttu-id="74d90-109">Описание</span><span class="sxs-lookup"><span data-stu-id="74d90-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="74d90-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="74d90-110">*SCode*</span></span> |<span data-ttu-id="74d90-111">Integer, который указывает код состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="74d90-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="74d90-112">*Описание*</span><span class="sxs-lookup"><span data-stu-id="74d90-112">*Description*</span></span> |<span data-ttu-id="74d90-113">**Строка,** которая указывает описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="74d90-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="74d90-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="74d90-114">*Source*</span></span> |<span data-ttu-id="74d90-115">**Строка,** которая указывает запрос или команду, которая вызвала ошибку.</span><span class="sxs-lookup"><span data-stu-id="74d90-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="74d90-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="74d90-116">*CancelDisplay*</span></span> |<span data-ttu-id="74d90-117">Значение **Boolean,** которое, если **задано значение True,** предотвращает отображение ошибки в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="74d90-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

