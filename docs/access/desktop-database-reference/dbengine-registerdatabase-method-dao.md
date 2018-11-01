---
title: DBEngine.RegisterDatabase Method (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fcb8e675f488c0d69f4c0d0b6329c47085d51e26
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888624"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="ca239-102">DBEngine.RegisterDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="ca239-102">DBEngine.RegisterDatabase Method (DAO)</span></span>


<span data-ttu-id="ca239-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca239-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ca239-104">Вводит сведения о подключении к источнику данных ODBC в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="ca239-104">Enters connection information for an ODBC data source in the Windows Registry.</span></span> <span data-ttu-id="ca239-105">Драйвер ODBC требуются данные подключения при открытии источника данных во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="ca239-105">The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca239-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca239-106">Syntax</span></span>

<span data-ttu-id="ca239-107">*выражение* . RegisterDatabase (***уведомления о доставке***, ***драйвер***, ***Автоматическая***, ***атрибуты***)</span><span class="sxs-lookup"><span data-stu-id="ca239-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="ca239-108">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="ca239-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="ca239-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca239-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca239-110">Имя</span><span class="sxs-lookup"><span data-stu-id="ca239-110">Name</span></span></p></th>
<th><p><span data-ttu-id="ca239-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="ca239-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ca239-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ca239-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ca239-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ca239-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca239-114">Уведомления о доставке</span><span class="sxs-lookup"><span data-stu-id="ca239-114">Dsn</span></span></p></td>
<td><p><span data-ttu-id="ca239-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca239-115">Required</span></span></p></td>
<td><p><span data-ttu-id="ca239-116"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="ca239-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ca239-117">имя, используемое в методе <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="ca239-117">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method.</span></span> <span data-ttu-id="ca239-118">Он ссылается на блок описательные сведения об источнике данных.</span><span class="sxs-lookup"><span data-stu-id="ca239-118">It refers to a block of descriptive information about the data source.</span></span> <span data-ttu-id="ca239-119">Например если источник данных ODBC удаленной базы данных, может быть имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ca239-119">For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca239-120">Драйвер</span><span class="sxs-lookup"><span data-stu-id="ca239-120">Driver</span></span></p></td>
<td><p><span data-ttu-id="ca239-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca239-121">Required</span></span></p></td>
<td><p><span data-ttu-id="ca239-122"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="ca239-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ca239-123">Имя драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="ca239-123">The name of the ODBC driver.</span></span> <span data-ttu-id="ca239-124">Это не имя DLL-файла драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="ca239-124">This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca239-125">Автоматическая</span><span class="sxs-lookup"><span data-stu-id="ca239-125">Silent</span></span></p></td>
<td><p><span data-ttu-id="ca239-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca239-126">Required</span></span></p></td>
<td><p><span data-ttu-id="ca239-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="ca239-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="ca239-128"><strong>Значение true,</strong> Если вы не хотите отображение диалоговых окон драйвера ODBC, запрашивающие сведения; или <strong>значение False,</strong> Если необходимо отобразить диалоговые окна драйвера ODBC.</span><span class="sxs-lookup"><span data-stu-id="ca239-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="ca239-129">Если автоматическая имеет <strong>значение True</strong>, атрибуты должно содержать все необходимые сведения или диалоговые окна отображаются все равно.</span><span class="sxs-lookup"><span data-stu-id="ca239-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca239-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca239-130">Attributes</span></span></p></td>
<td><p><span data-ttu-id="ca239-131">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca239-131">Required</span></span></p></td>
<td><p><span data-ttu-id="ca239-132"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="ca239-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ca239-133">Список ключевых слов для добавления к реестра Windows.</span><span class="sxs-lookup"><span data-stu-id="ca239-133">A list of keywords to be added to the Windows Registry.</span></span> <span data-ttu-id="ca239-134">Ключевые слова находятся в возврат каретки return – запятой строку.</span><span class="sxs-lookup"><span data-stu-id="ca239-134">The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ca239-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca239-135">Remarks</span></span>

<span data-ttu-id="ca239-136">Если база данных уже зарегистрирована (сведения о подключении к уже введены) в реестре Windows при использовании метода **RegisterDatabase** обновляется сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="ca239-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="ca239-137">В случае сбоя метода **RegisterDatabase** по любой причине никаких изменений не производится реестра Windows, и возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ca239-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="ca239-138">Дополнительные сведения о драйверы ODBC, такие как SQL Server файл справки, входящие в состав драйвера см.</span><span class="sxs-lookup"><span data-stu-id="ca239-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="ca239-139">Пример</span><span class="sxs-lookup"><span data-stu-id="ca239-139">Example</span></span>

<span data-ttu-id="ca239-140">В этом примере используется метод **RegisterDatabase** для регистрации источника данных Microsoft SQL Server с именем издателей в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="ca239-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

