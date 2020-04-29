---
title: Многопоточность и конфликты памяти в Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- Многопоточность в Excel, конфликты памяти в Excel, функции [Excel 2007], потокобезопасные и потокобезопасные функции [Excel 2007], локальная память потока [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301640"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Многопоточность и конфликты памяти в Excel

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Более ранние версии Microsoft Excel, чем Excel 2007, используют один поток для всех вычислений листа. Тем не менее, начиная с Excel 2007, в Excel можно настроить использование от 1 до 1024 параллельных потоков для вычисления листа. На многопроцессорном или многоядерном компьютере количество потоков по умолчанию равно числу процессоров или ядер. Таким образом, потокобезопасные ячейки или ячейки, содержащие только функции, которые являются потокобезопасными, могут быть выделены для параллельных потоков, подчиняются обычной логике пересчета, которую необходимо вычислить после их приоритетов.
  
## <a name="thread-safe-functions"></a>Потокобезопасные функции

Большинство встроенных функций листа, начиная с Excel 2007, являются потокобезопасными. Вы также можете записывать и регистрировать функции XLL как потокобезопасные. Excel использует один поток (основной поток), чтобы вызывать все команды, небезопасные функции, функции **xlAuto** (кроме [xlAutoFree](xlautofree-xlautofree12.md) и **xlAutoFree12**), а также функции COM и Visual Basic для приложений (VBA).
  
Где функция XLL возвращает **XLOPER** или **XLOPER12** с набором **кслбитдллфри** , Excel использует тот же поток, в котором был выполнен вызов функции для вызова **xlAutoFree** или **xlAutoFree12**. Вызов **xlAutoFree** или **xlAutoFree12** выполняется до следующего вызова функции в этом потоке. 
  
Для разработчиков XLL существуют преимущества для создания потокобезопасных функций:
  
- Они позволяют Excel максимально использовать многопроцессорный или многоядерный компьютер.
    
- Они открывают возможность использования удаленных серверов гораздо эффективнее, чем можно сделать с помощью одного потока.
    
Предположим, что у вас есть компьютер с одним процессором, на котором настроено использование, скажем, *N* потоков. Предположим, что электронная таблица работает с большим количеством вызовов функции XLL, которые в свою очередь отправляют запрос на данные или вычисление, выполняемое на удаленном сервере или кластере серверов. В зависимости от топологии дерева зависимостей Excel может вызвать функцию N раз почти одновременно. При условии, что сервер или серверы работают достаточно быстро или параллельно, время пересчета электронной таблицы может быть уменьшено до 1/N-кратного. 
  
Ключевая ошибка при написании потокобезопасных функций — корректно обрабатывает конфликты для ресурсов. Обычно это означает состязание за память и может быть разбито на две проблемы:
  
- Сведения о том, как создать память, которая будет использоваться только для этого потока.
    
- Обеспечение безопасного доступа к общей памяти несколькими потоками.
    
Первое, что следует знать о том, какой объем памяти XLL доступен всем потокам, и что доступно только в выполняемом в настоящий момент потоке.
  
 **Доступно всем потокам**
  
- Переменные, структуры и экземпляры классов, объявленные вне тела функции.
    
- Статические переменные, объявленные в теле функции.
    
В этих двух случаях память задается в блоке памяти DLL, созданном для этого экземпляра DLL. Если другой экземпляр приложения загружает библиотеку DLL, он получает собственную копию этой памяти, чтобы избежать конфликтов для этих ресурсов извне этого экземпляра DLL.
  
 **Доступно только текущему потоку**
  
- Автоматические переменные в коде функции (включая аргументы функции).
    
В этом случае память задается в стеке для каждого экземпляра вызова функции.
  
> [!NOTE]
> Область динамически выделяемой памяти зависит от области указателя, указывающей на него: если указатель доступен всем потокам, память также будет иметь. Если указатель является автоматической переменной в функции, выделенная память фактически является закрытой для этого потока. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Память, доступная только для одного потока: локальная память потока

С учетом того, что статические переменные в теле функции доступны всем потокам, функции, которые их используют, ясно являются потокобезопасными. Один экземпляр функции в одном потоке может изменить значение, в то время как другой экземпляр в другом потоке предполагается, что это совершенно другое. 
  
Объявить статические переменные в функции можно двумя причинами:
  
1. Статические данные можно хранить от одного вызова к другому.
    
2. Функция может безопасно возвратить указатель на статические данные.
    
В первую очередь вы можете использовать данные, которые хранятся и имеют значение для всех вызовов функции: возможно, простой счетчик, увеличивающийся каждый раз при вызове функции в любом потоке, или структура, собирающая данные об использовании и производительности при каждом вызове. Вопрос заключается в защите общих данных или структуры данных. Это лучше всего сделать с помощью критического раздела, как описано в следующем разделе.
  
Если данные предназначены только для этого потока, что может быть из-за случая 1 и всегда является основанием 2, то вопрос состоит в том, как создать память, которая сохраняется, но доступна только из этого потока. Одним из решений является использование API локальной памяти потока (TLS).
  
Например, рассмотрим функцию, которая возвращает указатель на **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Эта функция не является потокобезопасной, так как один поток может вернуть статическую **XLOPER12** , а другая перезаписать ее. Вероятность того, что это **произошло, еще** лучше, если она должна передаваться в **xlAutoFree12**. Одно решение состоит в том, чтобы выделить **XLOPER12**, вернуть указатель на него и реализовать **xlAutoFree12** , чтобы освободить память **XLOPER12** . Этот подход используется во многих примерах функций, показанных в разделе [Управление памятью в Excel](memory-management-in-excel.md).
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Такой подход проще реализовать, чем подход, описанный в следующем разделе, который основывается на API TLS, но у него есть некоторые недостатки. Сначала Excel должен вызвать **xlAutoFree**/ **xlAutoFree12** любого **типа возвращенной**/ **XLOPER12**. Во-вторых, возникла проблема при возврате параметра **XLOPER**/ **XLOPER12**s, который возвращает возвращаемое значение вызова функции обратного вызова C API. В параметре **XLOPER**/ **XLOPER12** может указываться память, которую необходимо освободить в Excel, но **XLOPER**/ **XLOPER12** сама по себе она должна быть освобождена таким же образом, как и выделенная. Если такая таблица **XLOPER**/ **должна использоваться** в качестве значения, возвращаемого функцией листа XLL, простой способ информирования **xlAutoFree**/ **xlAutoFree12** о необходимости освобождать оба указателя соответствующим образом. (Установка **кслбиткслфри** и **кслбитдллфри** не решает проблему, так как обработка **XLOPER/XLOPER12** в Excel с обоими наборами не определена и может изменяться от версии к версии.) Чтобы обойти эту проблему, XLL может выполнить глубокое копирование всех размещенных в Excel структур **и XLOPER12** , которые она возвращает на лист. 
  
Решение, которое не позволяет избежать этих **ограничений, заключается**в заполнении и возврате локальных данных, подходов, которые требуют, чтобы **xlAutoFree/xlAutoFree12** не освобождают сам указатель в **XLOPER/XLOPER12** . 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

Следующий вопрос заключается в том, как настраивать и извлекать локальную память потока, другими словами, как реализовать функцию **get_thread_local_xloper12** в предыдущем примере. Это выполняется с помощью API локального хранилища потока (TLS). Первым шагом является получение индекса TLS с помощью параметра **TlsAlloc**, который в конечном счете должен быть выпущен с помощью **тлсфри**. Оба варианта лучше всего выполняются из **DllMain**.
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

После получения индекса следующим шагом будет выделить блок памяти для каждого потока. [Документация по разработке Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) рекомендует делать это каждый раз, когда функция обратного вызова **DllMain** вызывается с помощью события **DLL_THREAD_ATTACH** , и освобождает память на каждом **DLL_THREAD_DETACH**. Тем не менее, следуя этим рекомендациям, Библиотека DLL сделает ненужную работу для потоков, не используемых для пересчета. 
  
Вместо этого лучше использовать стратегию выделения на основе первого использования. Сначала необходимо определить структуру, которую необходимо выделить для каждого потока. Для предыдущих примеров, которые возвращают **XLOPER** или **XLOPER12**, достаточно выполнить следующие задачи, но вы можете создать любую структуру, удовлетворяющую Вашим потребностям.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

Следующая функция получает указатель на локальный экземпляр потока или выделяет его, если это первый вызов.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Теперь можно увидеть, как получается локальная память **XLOPER/XLOPER12** потока: сначала вы получаете указатель на экземпляр **TLS_data**потока, а затем вернете указатель на **XLOPER/XLOPER12** , содержащийся в нем, как показано ниже. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Функции **mtr_safe_example_1** и **mtr_safe_example_2** могут быть зарегистрированы как потокобезопасные функции для работы с листом при запуске Excel. Однако вы не можете смешивать два подхода в одном XLL. XLL может экспортировать только одну реализацию **xlAutoFree** и **xlAutoFree12**, а каждая стратегия использования памяти требует различных подходов. При использовании **mtr_safe_example_1**указатель, передаваемый в **xlAutoFree/xlAutoFree12** , должен быть освобожден вместе с любыми данными, на которые они указывают. С **mtr_safe_example_2**только данные, указывающие на данные, должны быть освобождены.
  
Кроме того, Windows предоставляет функцию **жеткуррентсреадид**, которая возвращает уникальный системный идентификатор текущего потока. Это предоставляет разработчику еще один способ сделать код потокобезопасным, а также присвоить конкретному потоку поведение.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Память, доступная только для нескольких потоков: критические секции

Необходимо защитить память чтения/записи, к которой можно получить доступ из нескольких потоков, используя критические разделы. Для каждого блока памяти, который необходимо защитить, требуется именованный критический раздел. Вы можете инициализировать их во время вызова функции **xlAutoOpen** и освободить их и задать значение null при вызове функции **xlAutoClose** . Затем необходимо включить каждый доступ к защищенному блоку в пределах одной из двух вызовов **ентеркритикалсектион** и **леавекритикалсектион**. В любой момент времени в критический раздел может быть разрешен только один поток. Ниже приведен пример инициализации, неинициализации и использования раздела с именем **g_csSharedTable**.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Другой, возможно, более безопасный способ защиты блока памяти состоит в создании класса, который содержит собственные **critical_section** , а методы конструктора, деструктора и метода доступа отвечают за его использование. В этом подходе Добавлено преимущество защиты объектов, которые могут быть инициализированы до **xlAutoOpen** , или после вызова **xlAutoClose** , однако следует быть внимательным при создании слишком большого количества критически важных разделов и издержек операционной системы, которые будут создаваться. 
  
При наличии кода, который нуждается в одновременном доступе к нескольким блокам защищенной памяти, необходимо тщательно продумать порядок ввода и выхода критических разделов. Например, следующие две функции могут создать взаимоблокировку.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Если первая функция в одном потоке вводит **g_csSharedTableA** , а вторая — в другом потоке, **g_csSharedTableB**, оба потока зависают. Правильный подход состоит в том, чтобы войти в последовательный порядок и выйти в обратном порядке, как показано ниже.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Там, где это возможно, лучше всего использовать точку совместной работы с потоком, чтобы изолировать доступ к отдельным блокам, как показано ниже.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

При большом объеме конфликтов для общего ресурса, например, при частом коротком доступе к короткой длительности, следует рассмотреть возможность использования критической секции для прокрутки. Это методика, которая делает ожидание менее ресурсоемких ресурсов процессора. Для этого можно использовать **инитиализекритикалсектионандспинкаунт** при инициализации раздела или **сеткритикалсектионспинкаунт** после инициализации, чтобы задать количество циклов потока перед тем, как оно станет доступным. Операция ожидания является дорогим, поэтому она позволяет избежать этого, если ресурс освобождается. В системе с одним процессором счетчик прокруток фактически игнорируется, но вы можете указать его без ущерба. Диспетчер кучи памяти использует счетчик прокрутки 4000. Дополнительные сведения об использовании критических разделов можно найти в документации по пакету SDK для Windows SDK. 
  
## <a name="see-also"></a>См. также



[Управление памятью в Excel](memory-management-in-excel.md)
  
[Многопоточный пересчет в Excel](multithreaded-recalculation-in-excel.md)
  
[Функции диспетчера надстроек и интерфейса XLL](add-in-manager-and-xll-interface-functions.md)

