---
title: Свойство Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716007"
---
# <a name="handler-property-rds"></a><span data-ttu-id="4700c-102">Свойство Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="4700c-102">Handler property (RDS)</span></span>

<span data-ttu-id="4700c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4700c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4700c-104">Указывает имя программы настройки на сервере (обработчик), которая расширяет возможности [RDSServer.DataFactory](datafactory-object-rdsserver.md)и все параметры, используемые в *обработчик*.</span><span class="sxs-lookup"><span data-stu-id="4700c-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="4700c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4700c-105">Syntax</span></span>

<span data-ttu-id="4700c-106">*DataControl*. Обработчик = *строка*</span><span class="sxs-lookup"><span data-stu-id="4700c-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="4700c-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4700c-107">Parameters</span></span>

|<span data-ttu-id="4700c-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4700c-108">Parameter</span></span>|<span data-ttu-id="4700c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4700c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4700c-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="4700c-110">*DataControl*</span></span> |<span data-ttu-id="4700c-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="4700c-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="4700c-112">*String*</span><span class="sxs-lookup"><span data-stu-id="4700c-112">*String*</span></span> |<span data-ttu-id="4700c-113">**Строковое** значение, содержащее имя обработчика и любых параметров, все запятыми (например, «handlerName, parm1, parm2,..., parm *N*»).</span><span class="sxs-lookup"><span data-stu-id="4700c-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="4700c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4700c-114">Remarks</span></span>

<span data-ttu-id="4700c-115">Это свойство поддерживает настройки, функциональные возможности, необходимо задать свойство [CursorLocation](cursorlocation-property-ado.md) **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="4700c-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="4700c-116">Имя обработчика и ее параметры при их наличии, разделенных запятыми («,»).</span><span class="sxs-lookup"><span data-stu-id="4700c-116">The name of the handler and its parameters, if any, are separated by commas (",").</span></span> <span data-ttu-id="4700c-117">Непредсказуемое поведение приведет к, если точку с запятой («;») в любом месте отображается в *строке*.</span><span class="sxs-lookup"><span data-stu-id="4700c-117">Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*.</span></span> <span data-ttu-id="4700c-118">Можно создать собственный обработчик условии, что он поддерживает интерфейс **IDataFactoryHandler** .</span><span class="sxs-lookup"><span data-stu-id="4700c-118">You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="4700c-119">Имя обработчика по умолчанию — **MSDFMAP. Обработчик**, и его параметр по умолчанию — это файл настройки с именем **MSDFMAP. INI**.</span><span class="sxs-lookup"><span data-stu-id="4700c-119">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**.</span></span> <span data-ttu-id="4700c-120">Это свойство используется для вызова настройки альтернативного файлы, созданные администратором сервера.</span><span class="sxs-lookup"><span data-stu-id="4700c-120">Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="4700c-121">Альтернатива для установки свойства **обработчика** — указание обработчика и параметры в свойство [ConnectionString](connectionstring-property-ado.md) ; то есть «\**обработчик = \*\*\* handlerName, parm1, parm2,...;*«.</span><span class="sxs-lookup"><span data-stu-id="4700c-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

