---
title: Свойство TableDef. Ластупдатед (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308416"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="d425b-102">Свойство TableDef. Ластупдатед (DAO)</span><span class="sxs-lookup"><span data-stu-id="d425b-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="d425b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d425b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d425b-104">Возвращает дату и время последнего изменения, внесенного в объект.</span><span class="sxs-lookup"><span data-stu-id="d425b-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="d425b-105">Только для чтения, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="d425b-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d425b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d425b-106">Syntax</span></span>

<span data-ttu-id="d425b-107">*Expression* . ластупдатед</span><span class="sxs-lookup"><span data-stu-id="d425b-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="d425b-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="d425b-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d425b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d425b-109">Remarks</span></span>

<span data-ttu-id="d425b-110">**DateCreated** и **ластупдатед** возвращают дату и время создания или последнего обновления объекта.</span><span class="sxs-lookup"><span data-stu-id="d425b-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="d425b-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и Ластупдатед.</span><span class="sxs-lookup"><span data-stu-id="d425b-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

