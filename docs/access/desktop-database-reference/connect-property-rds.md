---
title: Подключение (RDS)
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
# <a name="connect-property-rds"></a><span data-ttu-id="bbb0b-102">Подключение (RDS)</span><span class="sxs-lookup"><span data-stu-id="bbb0b-102">Connect property (RDS)</span></span>

<span data-ttu-id="bbb0b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbb0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbb0b-104">Указывает имя базы данных, из которого запускаются операции запроса и обновления.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="bbb0b-105">Вы можете задать **Подключение** в момент разработки в [RDS. Объектные теги объекта DataControl](datacontrol-object-rds.md) или во время запуска в коде скриптов (например, VBScript).</span><span class="sxs-lookup"><span data-stu-id="bbb0b-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb0b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbb0b-106">Syntax</span></span>

<span data-ttu-id="bbb0b-107">Время разработки: \< PARAM NAME="Подключение" VALUE="ConnectionString"\></span><span class="sxs-lookup"><span data-stu-id="bbb0b-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="bbb0b-108">Время запуска: DataControl. Подключение = "ConnectionString"</span><span class="sxs-lookup"><span data-stu-id="bbb0b-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="bbb0b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbb0b-109">Parameters</span></span>

|<span data-ttu-id="bbb0b-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="bbb0b-110">Parameter</span></span>|<span data-ttu-id="bbb0b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="bbb0b-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bbb0b-112">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="bbb0b-112">*ConnectionString*</span></span> |<span data-ttu-id="bbb0b-113">Допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-113">A valid connection string.</span></span> <span data-ttu-id="bbb0b-114">Дополнительные сведения о строках подключения см. в свойстве [ConnectionString](connectionstring-property-ado.md) или документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-114">For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span><br/><br/><span data-ttu-id="bbb0b-115">**ПРИМЕЧАНИЕ.** Указание ms Remote в качестве поставщика для **RDS. DataControl** создаст четырехуровневый сценарий.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-115">**NOTE**: Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="bbb0b-116">Сценарии с более чем тремя уровнями не были протестированы и не должны быть необходимы.</span><span class="sxs-lookup"><span data-stu-id="bbb0b-116">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>|
|<span data-ttu-id="bbb0b-117">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="bbb0b-117">*DataControl*</span></span> |<span data-ttu-id="bbb0b-118">Переменная объекта, представляюая **RDS. Объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="bbb0b-118">An object variable that represents an **RDS.DataControl** object.</span></span>|

