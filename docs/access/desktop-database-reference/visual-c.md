---
title: Visual C++ (справочник по базам данных Access для настольных ПК)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 082790c33840bfeacf0c1a6bd38af34c0617f4fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303404"
---
# <a name="visual-c"></a><span data-ttu-id="54ed4-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="54ed4-102">Visual C++</span></span>


<span data-ttu-id="54ed4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54ed4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54ed4-104">Это схематическое описание того, как можно сделать события ADO в Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="54ed4-104">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++.</span></span> <span data-ttu-id="54ed4-105">Полное описание см. в примере модели событий [ADO (VC++).](ado-events-model-example-vc.md)</span><span class="sxs-lookup"><span data-stu-id="54ed4-105">See [ADO Events Model example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="54ed4-106">Создайте классы, производные от интерфейсов **ConnectionEventsVt** и **RecordsetEventsVt,** найденных в файле adoint.h.</span><span class="sxs-lookup"><span data-stu-id="54ed4-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

```cpp 
 
// BeginEventExampleVC01 
class CConnEvent : public ConnectionEventsVt 
{ 
 public: 
 STDMETHODIMP InfoMessage( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection); 
... 
} 
 
class CRstEvent : public RecordsetEventsVt 
{ 
 public: 
 STDMETHODIMP WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset); 
... 
} 
// EndEventExampleVC01 
```

<span data-ttu-id="54ed4-107">Реализуют каждый из методов обработки событий в обоих классах.</span><span class="sxs-lookup"><span data-stu-id="54ed4-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="54ed4-108">Достаточно, чтобы каждый метод просто возвращал HRESULT S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54ed4-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="54ed4-109">Однако когда вы сообщаете, что ваши обработчики событий доступны, они будут постоянно звыться по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="54ed4-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="54ed4-110">Вместо этого можно запросить большее уведомление после первого установки **adStatus** в **adStatusUnwantedEvent.**</span><span class="sxs-lookup"><span data-stu-id="54ed4-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

```cpp 
 
// BeginEventExampleVC02 
STDMETHODIMP CConnEvent::ConnectComplete( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
// EndEventExampleVC02 
```

<span data-ttu-id="54ed4-111">Классы событий наследуются от **IUnknown,** поэтому необходимо также реализовать методы **QueryInterface,** **AddRef** и **Release.**</span><span class="sxs-lookup"><span data-stu-id="54ed4-111">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods.</span></span> <span data-ttu-id="54ed4-112">Также реализуют конструкторы классов и деструкторы.</span><span class="sxs-lookup"><span data-stu-id="54ed4-112">Also implement class constructors and destructors.</span></span> <span data-ttu-id="54ed4-113">Выберите инструменты Visual C++, с помощью которых вам будет удобнее всего упростить эту часть задачи.</span><span class="sxs-lookup"><span data-stu-id="54ed4-113">Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="54ed4-114">Чтобы сделать обработчики событий доступными, выдайте **QueryInterface** в объектах [Recordset](recordset-object-ado.md) и [Connection](connection-object-ado.md) для интерфейсов **IConnectionPointContainer** и **IConnectionPoint.**</span><span class="sxs-lookup"><span data-stu-id="54ed4-114">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="54ed4-115">Затем **выдайте IConnectionPoint::Advise** для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="54ed4-115">Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="54ed4-116">Например, предположим, что используется логская функция, которая возвращает **true,** если объект **Recordset** успешно информирует о наличии доступных обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="54ed4-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

```cpp 
 
// BeginEventExampleVC03 
HRESULT hr; 
DWORD dwEvtClass; 
IConnectionPointContainer *pCPC = NULL; 
IConnectionPoint *pCP = NULL; 
CRstEvent *pRStEvent = NULL; 
... 
_RecordsetPtr pRs; 
pRs.CreateInstance(__uuidof(Recordset)); 
pRStEvent = new CRstEvent; 
if (pRStEvent == NULL) return FALSE; 
... 
hr = pRs->QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&pCPC); 
if (FAILED(hr)) return FALSE; 
hr = pCPC->FindConnectionPoint(RecordsetEvents, &pCP); 
pCPC->Release(); // Always Release now, even before checking. 
if (FAILED(hr)) return FALSE; 
hr = pCP->Advise(pRstEvent, &dwEvtClass); //Turn on event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
return TRUE; 
... 
// EndEventExampleVC03 
```

<span data-ttu-id="54ed4-117">На этом этапе события для семейства **RecordsetEvent** включены, и ваши методы будут вызваны по мере возникновения событий **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="54ed4-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="54ed4-118">Позже, чтобы сделать обработчики событий недоступными, снова получите точку подключения и выдайте метод **IConnectionPoint::Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="54ed4-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="54ed4-119">Необходимо освободить интерфейсы и уничтожать объекты классов соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="54ed4-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="54ed4-120">В следующем коде показан полный пример класса **recordset** Event sink.</span><span class="sxs-lookup"><span data-stu-id="54ed4-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

```vb 
 
// BeginEventExampleVC05 
#include <adoint.h> 
 
class CADORecordsetEvents : public RecordsetEventsVt 
{ 
public : 
 
 ULONG m_ulRefCount; 
 CADORecordsetEvents():m_ulRefCount(1){} 
 
 STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) 
 { 
 if (IsEqualIID(__uuidof(IUnknown), iid) || 
 IsEqualIID(__uuidof(RecordsetEventsVt), iid)) 
 { 
 *ppvObject = this; 
 return S_OK; 
 } 
 else 
 return E_NOINTERFACE; 
 } 
 
 STDMETHOD_(ULONG, AddRef)() 
 { 
 return m_ulRefCount++; 
 } 
 
 STDMETHOD_(ULONG, Release)() 
 { 
 if (--m_ulRefCount == 0) 
 { 
 delete this; 
 return 0; 
 } 
 else 
 return m_ulRefCount; 
 } 
 
 
 STDMETHOD(WillChangeField)( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FieldChangeComplete)( 
 LONG cFields, 
 VARIANT Fields, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(WillChangeRecord)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(RecordChangeComplete)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillChangeRecordset)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(RecordsetChangeComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillMove)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(MoveComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(EndOfRecordset)( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FetchProgress)( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(FetchComplete)( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
}; 
// EndEventExampleVC05 
```

