---
title: Свойство (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 191ef13d4d3c73bfbee50d72720d7e450376dd23
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862921"
---
# <a name="connect-property-rds"></a><span data-ttu-id="40dcb-102">Свойство (RDS)</span><span class="sxs-lookup"><span data-stu-id="40dcb-102">Connect Property (RDS)</span></span>


<span data-ttu-id="40dcb-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40dcb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40dcb-104">Указывает имя базы данных, из которой запускаются операций запросов и обновления.</span><span class="sxs-lookup"><span data-stu-id="40dcb-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="40dcb-105">Можно задать свойство **подключение** во время разработки в [RDS. DataControl](datacontrol-object-rds.md) теги OBJECT объекта, или во время выполнения в коде (например, VBScript) сценария.</span><span class="sxs-lookup"><span data-stu-id="40dcb-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="40dcb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40dcb-106">Syntax</span></span>

<span data-ttu-id="40dcb-107">Время разработки: \<параметров имя = значение «связь» = «ConnectionString»\></span><span class="sxs-lookup"><span data-stu-id="40dcb-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="40dcb-108">Во время выполнения: DataControl.Connect = «ConnectionString»</span><span class="sxs-lookup"><span data-stu-id="40dcb-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="40dcb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="40dcb-109">Parameters</span></span>

- <span data-ttu-id="40dcb-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="40dcb-110">*ConnectionString*</span></span>

  - <span data-ttu-id="40dcb-111">Это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="40dcb-111">A valid connection string.</span></span> <span data-ttu-id="40dcb-112">Более общие сведения о строках подключения отображаться со значением свойства [ConnectionString](connectionstring-property-ado.md) или документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="40dcb-112">For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="40dcb-113">Указание удаленного MS в качестве поставщика для **RDS. DataControl** бы создать сценарий четыре уровня.</span><span class="sxs-lookup"><span data-stu-id="40dcb-113">Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario.</span></span> <span data-ttu-id="40dcb-114">Сценарии, больше, чем три уровня не проверялись и не должно быть необходимым.</span><span class="sxs-lookup"><span data-stu-id="40dcb-114">Scenarios greater than three tiers have not been tested and should not be needed.</span></span>

- <span data-ttu-id="40dcb-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="40dcb-115">*DataControl*</span></span>

  - <span data-ttu-id="40dcb-116">Объектную переменную, которая представляет **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="40dcb-116">An object variable that represents an **RDS.DataControl** object.</span></span>

