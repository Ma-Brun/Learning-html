# Learning-html
tipo mierda



 <!-- <section class="todo">
                <h2>To‑Do List</h2>
                <div>
                        <input id="newItem" type="text" placeholder="Add item and press Add">
                        <button id="addBtn">Add</button>
                </div>
                <ul id="todoList"></ul>
        </section>

        <script>
        document.addEventListener('DOMContentLoaded', ()=> {
            const listEl = document.getElementById('todoList');
            const input = document.getElementById('newItem');
            const addBtn = document.getElementById('addBtn');

            function save(items){ localStorage.setItem('todoItems', JSON.stringify(items)); }
            function load(){ try{ return JSON.parse(localStorage.getItem('todoItems'))||[] }catch(e){return []} }

            function render(){
                listEl.innerHTML = '';
                load().forEach((it, idx) => {
                    const li = document.createElement('li');
                    if(it.done) li.classList.add('completed');
                    const span = document.createElement('span');
                    span.textContent = it.text;
                    const actions = document.createElement('span');
                    actions.className = 'item-actions';
                    const toggle = document.createElement('button');
                    toggle.textContent = it.done ? 'Undo' : 'Done';
                    toggle.addEventListener('click', ()=> {
                        const items = load(); items[idx].done = !items[idx].done; save(items); render();
                    });
                    const del = document.createElement('button');
                    del.textContent = 'Delete';
                    del.addEventListener('click', ()=> { const items = load(); items.splice(idx,1); save(items); render(); });
                    actions.appendChild(toggle); actions.appendChild(del);
                    li.appendChild(span); li.appendChild(actions);
                    listEl.appendChild(li);
                });
            }

            addBtn.addEventListener('click', ()=> {
                const v = input.value.trim(); if(!v) return;
                const items = load(); items.push({text:v, done:false}); save(items); input.value=''; render();
            });

            input.addEventListener('keydown', e=> { if(e.key==='Enter') addBtn.click(); });

            render();
        });
        </script> -->