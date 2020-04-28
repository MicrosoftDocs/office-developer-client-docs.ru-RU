---
title: Свойство Connect (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295984"
---
# <a name="connect-property-rds"></a><span data-ttu-id="41c2b-102">Свойство Connect (RDS)</span><span class="sxs-lookup"><span data-stu-id="41c2b-102">Connect property (RDS)</span></span>

<span data-ttu-id="41c2b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41c2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41c2b-104">Указывает имя базы данных, из которой выполняются операции запроса и обновления.</span><span class="sxs-lookup"><span data-stu-id="41c2b-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="41c2b-105">Свойство **Connect** можно задать во время создания в службе [RDS. Объектные теги объекта DataObject или](datacontrol-object-rds.md) во время выполнения в коде сценария (например, на языке VBScript).</span><span class="sxs-lookup"><span data-stu-id="41c2b-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="41c2b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41c2b-106">Syntax</span></span>

<span data-ttu-id="41c2b-107">Время конструирования \<: param Name = "Connect" value = "ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="41c2b-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="41c2b-108">Время выполнения: Control. Connect = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="41c2b-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="41c2b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="41c2b-109">Parameters</span></span>

|<span data-ttu-id="41c2b-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="41c2b-110">Parameter</span></span>|<span data-ttu-id="41c2b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="41c2b-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="41c2b-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="41c2b-112">*ConnectionString*</span></span> |<span data-ttu-id="41c2b-113">Допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="41c2b-113">A valid connection string.</span></span> <span data-ttu-id="41c2b-114">Более общие сведения о строках подключения приведены в статье свойство [ConnectionString](connectionstring-property-ado.md) или документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="41c2b-114">For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="41c2b-115">**Note**: указание MS Remote в качестве поставщика для **RDS. Элемент управления** "объект" создает сценарий из четырех уровней.</span><span class="sxs-lookup"><span data-stu-id="41c2b-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="41c2b-116">Сценарии с более чем тремя уровнями не тестировались и не должны быть необходимыми.</span><span class="sxs-lookup"><span data-stu-id="41c2b-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="41c2b-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="41c2b-117">*DataControl*</span></span> |<span data-ttu-id="41c2b-118">Объектная переменная, представляющая **RDS. Объект управления** DataObject.</span><span class="sxs-lookup"><span data-stu-id="41c2b-118">An object variable that represents an **RDS.DataControl** object.</span></span>|

