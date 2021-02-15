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
# <a name="handler-property-rds"></a><span data-ttu-id="a9253-102">Свойство Handler (RDS)</span><span class="sxs-lookup"><span data-stu-id="a9253-102">Handler property (RDS)</span></span>

<span data-ttu-id="a9253-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9253-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9253-104">Указывает имя программы настройки на стороне сервера (обработчика), которая расширяет функциональные возможности [RDSServer.DataFactory](datafactory-object-rdsserver.md)и любые параметры, используемые обработчиком. </span><span class="sxs-lookup"><span data-stu-id="a9253-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9253-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9253-105">Syntax</span></span>

<span data-ttu-id="a9253-106">*DataControl*. Handler = *String*</span><span class="sxs-lookup"><span data-stu-id="a9253-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="a9253-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9253-107">Parameters</span></span>

|<span data-ttu-id="a9253-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a9253-108">Parameter</span></span>|<span data-ttu-id="a9253-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a9253-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a9253-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="a9253-110">*DataControl*</span></span> |<span data-ttu-id="a9253-111">Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="a9253-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="a9253-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="a9253-112">*String*</span></span> |<span data-ttu-id="a9253-113">**Строковое** значение, которое содержит имя обработвода и все параметры, разделенные запятой (например, "handlerName,parm1,parm2,...,parm *N"*).</span><span class="sxs-lookup"><span data-stu-id="a9253-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="a9253-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="a9253-114">Remarks</span></span>

<span data-ttu-id="a9253-115">Это свойство поддерживает настройку, функциональность, требуемую установки свойству [CursorLocation](cursorlocation-property-ado.md) свойства **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="a9253-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="a9253-116">Имя обработера и его параметры(если таковые имеются) разделяются запятой (",").</span><span class="sxs-lookup"><span data-stu-id="a9253-116">The name of the handler and its parameters, if any, are separated by commas (",").</span></span> <span data-ttu-id="a9253-117">Непредсказуемое поведение приведет, если в строке появится точку с за точкой с зачетом *(";").*</span><span class="sxs-lookup"><span data-stu-id="a9253-117">Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*.</span></span> <span data-ttu-id="a9253-118">Можно написать собственный обработчик, если он поддерживает интерфейс **IDataFactoryHandler.**</span><span class="sxs-lookup"><span data-stu-id="a9253-118">You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="a9253-119">Имя обработера по умолчанию **— MSDFMAP. Обработок** и его параметр по умолчанию — это файл настройки **с именемMSDFMAP.INI.**</span><span class="sxs-lookup"><span data-stu-id="a9253-119">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**.</span></span> <span data-ttu-id="a9253-120">Это свойство используется для вызова альтернативных файлов настройки, созданных администратором сервера.</span><span class="sxs-lookup"><span data-stu-id="a9253-120">Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="a9253-121">В качестве альтернативы настройке **свойства Handler** можно указать обработок и параметры в [свойстве ConnectionString;](connectionstring-property-ado.md) то есть"\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="a9253-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

