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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292071"
---
# <a name="handler-property-rds"></a><span data-ttu-id="67644-102">Свойство Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="67644-102">Handler property (RDS)</span></span>

<span data-ttu-id="67644-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67644-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67644-104">Указывает имя программы настройки на стороне сервера (обработчика), расширяющей функциональные возможности [рдссервер.](datafactory-object-rdsserver.md), и все параметры, используемые *обработчиком*.</span><span class="sxs-lookup"><span data-stu-id="67644-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="67644-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67644-105">Syntax</span></span>

<span data-ttu-id="67644-106">*Элемент управления*. Обработчик = *строка*</span><span class="sxs-lookup"><span data-stu-id="67644-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="67644-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="67644-107">Parameters</span></span>

|<span data-ttu-id="67644-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="67644-108">Parameter</span></span>|<span data-ttu-id="67644-109">Описание</span><span class="sxs-lookup"><span data-stu-id="67644-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="67644-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="67644-110">*DataControl*</span></span> |<span data-ttu-id="67644-111">Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="67644-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="67644-112">*String*</span><span class="sxs-lookup"><span data-stu-id="67644-112">*String*</span></span> |<span data-ttu-id="67644-113">**Строковое** значение, содержащее имя обработчика и все параметры, разделенные запятыми (например, "хандлернаме, parm1, parm2,..., ПАРМ *N*").</span><span class="sxs-lookup"><span data-stu-id="67644-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="67644-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="67644-114">Remarks</span></span>

<span data-ttu-id="67644-115">Это свойство поддерживает настройку, которая требует установки свойства [CursorLocation](cursorlocation-property-ado.md) в **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="67644-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="67644-116">Имя обработчика и его параметры разделяются запятыми (",").</span><span class="sxs-lookup"><span data-stu-id="67644-116">The name of the handler and its parameters, if any, are separated by commas (",").</span></span> <span data-ttu-id="67644-117">Непредсказуемое поведение приведет к появлению точки с запятой (";") в любом месте *строки*.</span><span class="sxs-lookup"><span data-stu-id="67644-117">Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*.</span></span> <span data-ttu-id="67644-118">Вы можете написать собственный обработчик, при условии, что он поддерживает интерфейс **идатафакторихандлер** .</span><span class="sxs-lookup"><span data-stu-id="67644-118">You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="67644-119">Имя обработчика по умолчанию — **мсдфмап. , А**его параметр по умолчанию — файл настройки с именем **мсдфмап. INI**.</span><span class="sxs-lookup"><span data-stu-id="67644-119">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**.</span></span> <span data-ttu-id="67644-120">Используйте это свойство, чтобы вызвать альтернативные файлы настройки, созданные администратором сервера.</span><span class="sxs-lookup"><span data-stu-id="67644-120">Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="67644-121">Альтернативой заданию свойства **handler** является указание обработчика и параметров в свойстве [ConnectionString](connectionstring-property-ado.md) ; то есть "\**handler = \* \* \* хандлернаме, parm1, parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="67644-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

