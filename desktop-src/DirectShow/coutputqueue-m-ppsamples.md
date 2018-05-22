---
Description: 'Array of samples of size COutputQueue::m\_lBatchSize.'
ms.assetid: '5c4b904d-480b-4393-a799-63989669ea1c'
title: 'COutputQueue::m\_ppSamples member'
---

# COutputQueue::m\_ppSamples member

Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).

## Syntax


```C++
IMediaSample **m_ppSamples;
```



## Remarks

The worker thread pulls samples from the queue and places them in this array. It passes the array to the [**IMemInputPin::ReceiveMultiple**](imeminputpin-receivemultiple.md) method. If the object is not using a worker thread, the object places samples directly into this array. The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.

## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**COutputQueue Class**](coutputqueue.md)
</dt> </dl>

�

�



