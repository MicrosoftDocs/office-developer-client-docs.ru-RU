---
title: Событие onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c67e277c35e3cf6c75226dc138aa4b288843e6bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930863"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="e8374-102">Событие onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="e8374-102">onError event (RDS)</span></span>


<span data-ttu-id="e8374-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8374-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8374-104">События **onError** вызывается каждый раз, когда возникает ошибка во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e8374-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8374-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8374-105">Syntax</span></span>

<span data-ttu-id="e8374-106">onError*SCode* *Описание* *источника* *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="e8374-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="e8374-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8374-107">Parameters</span></span>

  - <span data-ttu-id="e8374-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="e8374-108">*SCode*</span></span>

  - <span data-ttu-id="e8374-109">Целое число, указывающее код состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="e8374-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="e8374-110">*Описание*</span><span class="sxs-lookup"><span data-stu-id="e8374-110">*Description*</span></span>

  - <span data-ttu-id="e8374-111">**Строка** , указывающая описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="e8374-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="e8374-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="e8374-112">*Source*</span></span>

  - <span data-ttu-id="e8374-113">**Строка** , указывающая запроса или команды, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="e8374-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="e8374-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="e8374-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="e8374-115">**Логическое** значение, которая, в случае присвоено **значение True**, который запрещает отображение в диалоговом окне ошибки.</span><span class="sxs-lookup"><span data-stu-id="e8374-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

