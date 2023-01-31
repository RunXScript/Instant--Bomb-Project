## 🛰 About
Really Fast Time Bomb Exploit For CSGO

## 🌌 Setup
- Create Doc Paste Txt
- Copy/Cut Doc
- Paste Into CSGO
- Run CSGO
- Enable Exploit Before Joining Match

## 🗿 Disclaimer
Software Contain Virus Because This Is A Cheat Program

## Software Download
Instant Bomb Exploit Copy Down Below
```ruby
	int simulation_ticks = DetermineSimulationTicks();
 
	// If some time will elapse, make sure our clock (m_nTickBase) starts at the correct time
	if ( simulation_ticks > 0 )
	{
		AdjustPlayerTimeBase( simulation_ticks );
	}



int CBasePlayer::DetermineSimulationTicks( void )
{
	int command_context_count = GetCommandContextCount();
 
	int context_number;
 
	int simulation_ticks = 0;
 
	// Determine how much time we will be running this frame and fixup player clock as needed
	for ( context_number = 0; context_number < command_context_count; context_number++ )
	{
		CCommandContext const *ctx = GetCommandContext( context_number );
		Assert( ctx );
		Assert( ctx->numcmds > 0 );
		Assert( ctx->dropped_packets >= 0 );
 
		// Determine how long it will take to run those packets
		simulation_ticks += ctx->numcmds + ctx->dropped_packets;
	}
 
	return simulation_ticks;
}





	m_LastCmd = ctx->cmds[ CMD_MOSTRECENT ];




else if ( bRunNullCmd )
	{
		CUserCmd cmd = m_LastCmd;	
 
		float flOldFrametime = gpGlobals->frametime;
		float flOldCurtime = gpGlobals->curtime;
 
		pl.fixangle = FIXANGLE_NONE;
		cmd.viewangles = EyeAngles();
 
                // this isnt done in current csgo source anymore, it just sets cmd->tickcount = gpGlobals->tickcount;
		float flTimeBase = gpGlobals->curtime;
		SetTimeBase( flTimeBase );
 
		MoveHelperServer()->SetHost( this );
		PlayerRunCommand( &cmd, MoveHelperServer() );
 
		SetLastUserCommand( cmd );
 
		// Restore the globals..
		gpGlobals->frametime = flOldFrametime;
		gpGlobals->curtime = flOldCurtime;
 
		MoveHelperServer()->SetHost( NULL );
	}







struct clc_msg_move_t
	{
		PAD( 0xc );
		int backup_commands;
		int num_commands;
	};
 
if ( primordial::exploits::time_shift() )
		{
			//printf( "overriding\n" );
			move_msg->num_commands = 0;
			move_msg->backup_commands = 1;
 
                        // this isnt necessarily needed but it makes sure that dropped_packets is 0 at all times, classy was having issues with this probably cuz of shit internet
                        csgo::client_state->net_chan()->choked_commands = 200;
		}



if ( primordial::exploits::time_shift() )
				cmd->viewangles = csgo::local()->get_eye_angles();
```
Instant Defuse Exploit Copy Down Below
```ruby
Patched Bruh
```
