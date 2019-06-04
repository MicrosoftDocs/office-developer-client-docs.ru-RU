---
title: Свойство Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 06/04/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 43afbfda8c560eafb90e6a53d85207e19e5b1170
ms.sourcegitcommit: 4a570873914c58dd4cdbe97b5d9ec41866dc797c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2019
ms.locfileid: "34675752"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="774c8-102">Свойство Recordset.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="774c8-102">Recordset.Filter property (DAO)</span></span>

<span data-ttu-id="774c8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="774c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="774c8-104">Задает или возвращает значение, определяющее записи, включаемые в открытый впоследствии объект **Recordset** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="774c8-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="774c8-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="774c8-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="774c8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="774c8-106">Syntax</span></span>

<span data-ttu-id="774c8-107">*выражение*.**Filter**</span><span class="sxs-lookup"><span data-stu-id="774c8-107">expression .Filter</span></span>

<span data-ttu-id="774c8-108">*выражение*: выражение, возвращающее объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="774c8-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="774c8-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="774c8-109">Remarks</span></span>

<span data-ttu-id="774c8-110">Параметр или возвращаемое значение является строковым типом данных, содержащим предложение WHERE оператора SQL без зарезервированного слова WHERE.</span><span class="sxs-lookup"><span data-stu-id="774c8-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="774c8-111">Используйте свойство **Filter**, чтобы применить фильтр к объекту **Recordset** типа динамический набор, статический набор или однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="774c8-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="774c8-112">Свойство **Filter** можно использовать для ограничения записей, возвращаемых из существующего объекта, если новый объект **Recordset** открыт на основе существующего объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="774c8-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="774c8-113">Используйте формат даты, принятый в США (месяц, день, год), при фильтрации полей, содержащих даты, даже если не используется версия ядра СУБД Microsoft Access для США (в этом случае необходимо вручную создать даты, сцепляя строки. Например: strMonth & "-" & strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="774c8-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="774c8-114">В противном случае данные могут не отфильтроваться нужным образом.</span><span class="sxs-lookup"><span data-stu-id="774c8-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="774c8-115">Во многих случаях быстрее будет открыть новый объект **Recordset** с помощью оператора SQL, который включает предложение WHERE.</span><span class="sxs-lookup"><span data-stu-id="774c8-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="774c8-116">Если свойству присвоено значение строки, объединенной с нецелочисленным значением, а параметры системы содержат десятичные символы, не используемые в США, например, запятую (пример, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), возникает ошибка при попытке открытия следующего объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="774c8-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="774c8-117">Это возникает по причине того, что при объединении число будет преобразовано в строку с помощью используемого по умолчанию в вашей системе десятичного символа, а SQL Microsoft Access поддерживает только десятичные символы, используемые в США.</span><span class="sxs-lookup"><span data-stu-id="774c8-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="774c8-118">Пример</span><span class="sxs-lookup"><span data-stu-id="774c8-118">Example</span></span>

<span data-ttu-id="774c8-119">В примере ниже показано, как использовать свойство Filter для определения записей, которые нужно включить в открываемый впоследствии объект Recordset.</span><span class="sxs-lookup"><span data-stu-id="774c8-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="774c8-120">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="774c8-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rst = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
