---
title: Visual C++ (Справочник по для настольных баз данных Access)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e6f0e020373db9bf0fe7acc1b1c7bfeab210329
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861423"
---
# <a name="visual-c"></a><span data-ttu-id="be69e-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="be69e-102">Visual C++</span></span>


<span data-ttu-id="be69e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="be69e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="be69e-104">Это Схематическое Описание способа для создания экземпляра ADO событий в Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="be69e-104">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++.</span></span> <span data-ttu-id="be69e-105">В разделе [пример модели событий ADO (VC ++)](ado-events-model-example-vc.md) полное описание.</span><span class="sxs-lookup"><span data-stu-id="be69e-105">See [ADO Events Model example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="be69e-106">Создайте классы, производные от **ConnectionEventsVt** и **RecordsetEventsVt** интерфейсов, обнаруженных в файл adoint.h.</span><span class="sxs-lookup"><span data-stu-id="be69e-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

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

<span data-ttu-id="be69e-107">Реализация каждого из методов обработчика событий в обоих классов.</span><span class="sxs-lookup"><span data-stu-id="be69e-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="be69e-108">Достаточно, что каждый метод просто возвращает значение HRESULT S\_кнопку ОК.</span><span class="sxs-lookup"><span data-stu-id="be69e-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="be69e-109">Тем не менее, если вы сделаете известных, что доступны обработчики событий, они будут называться постоянно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be69e-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="be69e-110">Вместо этого необходимо запросить уведомление не дальнейший после первого, параметр **adStatus** для **adStatusUnwantedEvent**.</span><span class="sxs-lookup"><span data-stu-id="be69e-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

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

<span data-ttu-id="be69e-111">Классы событий наследовать от **IUnknown**, необходимо реализовать **QueryInterface**, **AddRef**и методов **Release** .</span><span class="sxs-lookup"><span data-stu-id="be69e-111">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods.</span></span> <span data-ttu-id="be69e-112">Также можно реализуйте конструкторы и деструкторы классов.</span><span class="sxs-lookup"><span data-stu-id="be69e-112">Also implement class constructors and destructors.</span></span> <span data-ttu-id="be69e-113">Выбор средств Visual C++, с которыми вы умеете наиболее для упрощения этой части задачи.</span><span class="sxs-lookup"><span data-stu-id="be69e-113">Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="be69e-114">Сделать его известные, обработчики событий, доступны с помощью **QueryInterface** на [набор записей](recordset-object-ado.md) и объекты [подключения](connection-object-ado.md) для **IConnectionPointContainer** и **IConnectionPoint** интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="be69e-114">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="be69e-115">Затем заключать **IConnectionPoint::Advise** для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="be69e-115">Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="be69e-116">Например предположим, что вы используете логической функции, что возвращает **значение True,** если он успешно информирует **записей** объекта, что у вас есть обработчики событий недоступны.</span><span class="sxs-lookup"><span data-stu-id="be69e-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

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

<span data-ttu-id="be69e-117">На этом этапе события для семейства **RecordsetEvent** включены и методов будет вызываться при возникновении событий **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="be69e-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="be69e-118">Более поздних версий когда требуется сделать недоступным обработчики событий, снова получите точку подключения и заключать метода **IConnectionPoint::Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="be69e-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="be69e-119">Необходимо освободить интерфейсы и уничтожения объектов класса соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="be69e-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="be69e-120">Ниже приведен пример класса приемника событий **записей** .</span><span class="sxs-lookup"><span data-stu-id="be69e-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

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

